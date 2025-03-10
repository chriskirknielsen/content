---
title: SVGNumberList
slug: Web/API/SVGNumberList
page-type: web-api-interface
tags:
  - API
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGNumberList
---

{{APIRef("SVG")}}

## SVG number list interface

The `SVGNumberList` defines a list of {{ domxref("SVGNumber") }} objects.

An `SVGNumberList` object can be designated as read only, which means that attempts to modify the object will result in an exception being thrown.

An `SVGNumberList` is indexable and can be accessed like an array.

### Interface overview

<table class="standard-table">
  <tbody>
    <tr>
      <th scope="row">Also implement</th>
      <td>None</td>
    </tr>
    <tr>
      <th scope="row">Methods</th>
      <td>
        <ul>
          <li><code>void clear()</code></li>
          <li>
            {{ domxref("SVGNumber") }}
            <code
              >initialize(in {{ domxref("SVGNumber") }}
              <var>newItem</var>)</code
            >
          </li>
          <li>
            {{ domxref("SVGNumber") }}
            <code>getItem(in unsigned long <var>index</var>)</code>
          </li>
          <li>
            {{ domxref("SVGNumber") }}
            <code
              >insertItemBefore(in {{ domxref("SVGNumber") }}
              <var>newItem</var>, in unsigned long <var>index</var>)</code
            >
          </li>
          <li>
            {{ domxref("SVGNumber") }}
            <code
              >replaceItem(in {{ domxref("SVGNumber") }}
              <var>newItem</var>, in unsigned long <var>index</var>)</code
            >
          </li>
          <li>
            {{ domxref("SVGNumber") }}
            <code>removeItem(in unsigned long <var>index</var>)</code>
          </li>
          <li>
            {{ domxref("SVGNumber") }}
            <code
              >appendItem(in {{ domxref("SVGNumber") }}
              <var>newItem</var>)</code
            >
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Properties</th>
      <td>
        <ul>
          <li>readonly unsigned long <code>numberOfItems</code></li>
          <li>
            readonly unsigned long
            <code>length</code> {{ non-standard_inline() }}
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <th scope="row">Normative document</th>
      <td>
        <a href="https://www.w3.org/TR/SVG/types.html#InterfaceSVGNumberList"
          >SVG 1.1 (2nd Edition)</a
        >
      </td>
    </tr>
  </tbody>
</table>

## Properties

| Name                                          | Type          | Description                      |
| --------------------------------------------- | ------------- | -------------------------------- |
| `numberOfItems`                               | unsigned long | The number of items in the list. |
| `length` {{ non-standard_inline() }} | unsigned long | The number of items in the list. |

## Methods

<table class="standard-table">
  <thead>
    <tr>
      <th>Name &#x26; Arguments</th>
      <th>Return</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code><strong>clear</strong>()</code>
      </td>
      <td><var>void</var></td>
      <td>
        <p>
          Clears all existing current items from the list, with the result being
          an empty list.
        </p>
        <p><strong>Exceptions:</strong></p>
        <ul>
          <li>
            a {{ domxref("DOMException") }} with code
            <code>NO_MODIFICATION_ALLOWED_ERR</code> is raised when the list
            corresponds to a read only attribute or when the object itself is
            read only.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <code
          ><strong>initialize</strong>(in {{ domxref("SVGNumber") }}
          <var>newItem</var>)</code
        >
      </td>
      <td>{{ domxref("SVGNumber") }}</td>
      <td>
        <p>
          Clears all existing current items from the list and re-initializes the
          list to hold the single item specified by
          <code><var>newItem</var></code
          >. If the inserted item is already in a list, it is removed from its
          previous list before it is inserted into this list. The inserted item
          is the item itself and not a copy. The return value is the item
          inserted into the list.
        </p>
        <p><strong>Exceptions:</strong></p>
        <ul>
          <li>
            a {{ domxref("DOMException") }} with code
            <code>NO_MODIFICATION_ALLOWED_ERR</code> is raised when the list
            corresponds to a read only attribute or when the object itself is
            read only.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <code><strong>getItem</strong>(in unsigned long <var>index</var>)</code>
      </td>
      <td>{{ domxref("SVGNumber") }}</td>
      <td>
        <p>
          Returns the specified item from the list. The returned item is the
          item itself and not a copy. Any changes made to the item are
          immediately reflected in the list. The first item is
          number <code>0</code>.
        </p>
        <p><strong>Exceptions:</strong></p>
        <ul>
          <li>
            a {{ domxref("DOMException") }} with code
            <code>NO_MODIFICATION_ALLOWED_ERR</code> is raised when the list
            corresponds to a read only attribute or when the object itself is
            read only.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <code
          ><strong>insertItemBefore</strong>(in
          {{ domxref("SVGNumber") }} <var>newItem</var>, in unsigned
          long <var>index</var>)</code
        >
      </td>
      <td>{{ domxref("SVGNumber") }}</td>
      <td>
        <p>
          Inserts a new item into the list at the specified position. The first
          item is number <code>0</code>.
        </p>
        <p>
          If <code><var>newItem</var></code> is already in a list, it is removed
          from its previous list before it is inserted into this list. The
          inserted item is the item itself and not a copy. If the item is
          already in this list, note that the index of the item to insert before
          is before the removal of the item.
        </p>
        <p>
          If the <code><var>index</var></code> is equal to <code>0</code>, then
          the new item is inserted at the front of the list. If the index is
          greater than or equal to <code>numberOfItems</code>, then the new item
          is appended to the end of the list.
        </p>
        <p><strong>Exceptions:</strong></p>
        <ul>
          <li>
            a {{ domxref("DOMException") }} with code
            <code>NO_MODIFICATION_ALLOWED_ERR</code> is raised when the list
            corresponds to a read only attribute or when the object itself is
            read only.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <code
          ><strong>replaceItem</strong>(in {{ domxref("SVGNumber") }}
          <var>newItem</var>, in unsigned long <var>index</var>)</code
        >
      </td>
      <td>{{ domxref("SVGNumber") }}</td>
      <td>
        <p>
          Replaces an existing item in the list with a new item. If
          <code><var>newItem</var></code> is already in a list, it is removed
          from its previous list before it is inserted into this list. The
          inserted item is the item itself and not a copy. If the item is
          already in this list, note that the index of the item to replace is
          before the removal of the item.
        </p>
        <p><strong>Exceptions:</strong></p>
        <ul>
          <li>
            a {{ domxref("DOMException") }} with code
            <code>NO_MODIFICATION_ALLOWED_ERR</code> is raised when the list
            corresponds to a read only attribute or when the object itself is
            read only.
          </li>
          <li>
            a {{ domxref("DOMException") }} with code
            <code>INDEX_SIZE_ERR</code> is raised if
            <code><var>index</var></code
            > is greater than or equal to <code>numberOfItems</code>.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <code
          ><strong>removeItem</strong>(in unsigned long <var>index</var>)</code
        >
      </td>
      <td>{{ domxref("SVGNumber") }}</td>
      <td>
        <p>Removes an existing item from the list.</p>
        <p><strong>Exceptions:</strong></p>
        <ul>
          <li>
            a {{ domxref("DOMException") }} with code
            <code>NO_MODIFICATION_ALLOWED_ERR</code> is raised when the list
            corresponds to a read only attribute or when the object itself is
            read only.
          </li>
          <li>
            a {{ domxref("DOMException") }} with code
            <code>INDEX_SIZE_ERR</code> is raised if
            <code><var>index</var></code
            > is greater than or equal to <code>numberOfItems</code>.
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <code
          ><strong>appendItem</strong>(in {{ domxref("SVGNumber") }}
          <var>newItem</var>)</code
        >
      </td>
      <td>{{ domxref("SVGNumber") }}</td>
      <td>
        <p>
          Inserts a new item at the end of the list. If
          <code><var>newItem</var></code> is already in a list, it is removed
          from its previous list before it is inserted into this list. The
          inserted item is the item itself and not a copy.
        </p>
        <p><strong>Exceptions:</strong></p>
        <ul>
          <li>
            a {{ domxref("DOMException") }} with code
            <code>NO_MODIFICATION_ALLOWED_ERR</code> is raised when the list
            corresponds to a read only attribute or when the object itself is
            read only.
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Browser compatibility

{{Compat}}
