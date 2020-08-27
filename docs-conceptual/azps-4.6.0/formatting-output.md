---
title: Formattare l'output dei cmdlet di Azure PowerShell
description: Come formattare l'output dei cmdlet per Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.openlocfilehash: dbce06569ada169cdd93ae85d40e1554a7f7fdec
ms.sourcegitcommit: b94a3f00c147144b0ef7f8cf8d0f151e04674b89
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/25/2020
ms.locfileid: "88821821"
---
# <a name="format-azure-powershell-cmdlet-output"></a><span data-ttu-id="ea8d2-103">Formattare l'output dei cmdlet di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ea8d2-103">Format Azure PowerShell cmdlet output</span></span>

<span data-ttu-id="ea8d2-104">Per impostazione predefinita, ogni cmdlet di Azure PowerShell formatta l'output in modo da semplificarne la lettura.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="ea8d2-105">PowerShell consente di convertire o formattare l'output dei cmdlet inviandolo tramite pipe a uno dei cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea8d2-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="ea8d2-106">Formattazione</span><span class="sxs-lookup"><span data-stu-id="ea8d2-106">Formatting</span></span>      | <span data-ttu-id="ea8d2-107">Conversione</span><span class="sxs-lookup"><span data-stu-id="ea8d2-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="ea8d2-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="ea8d2-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="ea8d2-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="ea8d2-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="ea8d2-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="ea8d2-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="ea8d2-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="ea8d2-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="ea8d2-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="ea8d2-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="ea8d2-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="ea8d2-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="ea8d2-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="ea8d2-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="ea8d2-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="ea8d2-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="ea8d2-116">La formattazione viene usata per la visualizzazione in un terminale di PowerShell e la conversione viene usata per generare dati in modo che possano essere utilizzati da altri script o programmi.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="ea8d2-117">Formato dell'output della tabella</span><span class="sxs-lookup"><span data-stu-id="ea8d2-117">Table output format</span></span>

<span data-ttu-id="ea8d2-118">Per impostazione predefinita, i cmdlet di Azure PowerShell generano l'output in formato tabella.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="ea8d2-119">Questo formato non visualizza tutte le informazioni della risorsa richiesta:</span><span class="sxs-lookup"><span data-stu-id="ea8d2-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="ea8d2-120">La quantità di dati visualizzati da `Format-Table` può dipendere dalla larghezza della finestra della sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="ea8d2-121">Per limitare l'output a proprietà specifiche e ordinarle, i nomi di proprietà possono essere forniti come argomenti a `Format-Table`:</span><span class="sxs-lookup"><span data-stu-id="ea8d2-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="ea8d2-122">Formato di output elenco</span><span class="sxs-lookup"><span data-stu-id="ea8d2-122">List output format</span></span>

<span data-ttu-id="ea8d2-123">Il formato di output elenco restituisce due colonne, ovvero i nomi di proprietà seguiti dal valore.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="ea8d2-124">Per gli oggetti complessi, invece, viene visualizzato il tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="ea8d2-125">L'output seguente include alcuni campi rimossi.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="ea8d2-126">Analogamente a `Format-Table`, i nomi delle proprietà possono essere forniti per ordinare e limitare l'output:</span><span class="sxs-lookup"><span data-stu-id="ea8d2-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="ea8d2-127">Formato di output largo</span><span class="sxs-lookup"><span data-stu-id="ea8d2-127">Wide output format</span></span>

<span data-ttu-id="ea8d2-128">Il formato di output largo restituisce un solo nome di proprietà per query.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="ea8d2-129">È possibile controllare la proprietà da visualizzare specificando una proprietà come argomento.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="ea8d2-130">Formato di output personalizzato</span><span class="sxs-lookup"><span data-stu-id="ea8d2-130">Custom output format</span></span>

<span data-ttu-id="ea8d2-131">Il tipo di output `Custom-Format` viene usato per la formattazione di oggetti personalizzati.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="ea8d2-132">Senza argomenti si comporta come `Format-List` ma visualizza i nomi delle proprietà delle classi personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="ea8d2-133">L'output seguente include alcuni campi rimossi.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="ea8d2-134">Fornendo i nomi delle proprietà come argomenti a `Custom-Format`, si visualizzano come valori le coppie proprietà/valore per il set di oggetti personalizzati:</span><span class="sxs-lookup"><span data-stu-id="ea8d2-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="ea8d2-135">L'output seguente include alcuni campi rimossi.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="ea8d2-136">Conversione in altri formati di dati</span><span class="sxs-lookup"><span data-stu-id="ea8d2-136">Conversion to other data formats</span></span>

<span data-ttu-id="ea8d2-137">La famiglia `ConvertTo-*` di cmdlet consente di convertire i risultati dei cmdlet di Azure PowerShell in formati leggibili dal computer.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="ea8d2-138">Per ottenere solo alcune proprietà dai risultati di Azure PowerShell, usare il comando `Select-Object` in una pipe prima di eseguire la conversione.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="ea8d2-139">Gli esempi seguenti illustrano i diversi tipi di output restituiti da ogni conversione.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="ea8d2-140">Conversione in formato CSV</span><span class="sxs-lookup"><span data-stu-id="ea8d2-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="ea8d2-141">Conversione in formato JSON</span><span class="sxs-lookup"><span data-stu-id="ea8d2-141">Conversion to JSON</span></span>

<span data-ttu-id="ea8d2-142">L'output JSON non espande tutte le proprietà per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="ea8d2-143">Per modificare la profondità delle proprietà espanse, usare l'argomento `-Depth`.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="ea8d2-144">Per impostazione predefinita, la profondità di espansione è `2`.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="ea8d2-145">L'output seguente include alcuni campi rimossi.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="ea8d2-146">Conversione in formato XML</span><span class="sxs-lookup"><span data-stu-id="ea8d2-146">Conversion to XML</span></span>

<span data-ttu-id="ea8d2-147">Il cmdlet `ConvertTo-XML` converte l'oggetto risposta di Azure PowerShell in un oggetto XML puro, che può essere gestito come qualsiasi altro oggetto XML all'interno di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="ea8d2-148">Conversione in formato HTML</span><span class="sxs-lookup"><span data-stu-id="ea8d2-148">Conversion to HTML</span></span>

<span data-ttu-id="ea8d2-149">La conversione di un oggetto in formato HTML restituisce un output di cui verrà eseguito il rendering come formato tabella HTML.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="ea8d2-150">Il rendering del formato HTML dipende dal comportamento del browser per il rendering delle tabelle che non contengono alcuna informazione di larghezza.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="ea8d2-151">Non viene espanso alcun oggetto delle classi personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ea8d2-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```
