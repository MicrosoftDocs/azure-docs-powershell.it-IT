---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 56ac931259de9705e0d6703e1387853aba77b028
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004078"
---
# <span data-ttu-id="67b73-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="67b73-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="67b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67b73-102">SYNOPSIS</span></span>
<span data-ttu-id="67b73-103">Percorsi di test nell'Hub IoT</span><span class="sxs-lookup"><span data-stu-id="67b73-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="67b73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67b73-104">SYNTAX</span></span>

### <span data-ttu-id="67b73-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67b73-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b73-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="67b73-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b73-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="67b73-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67b73-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="67b73-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b73-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="67b73-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67b73-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="67b73-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b73-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="67b73-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67b73-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67b73-112">DESCRIPTION</span></span>
<span data-ttu-id="67b73-113">Testare un percorso specifico.</span><span class="sxs-lookup"><span data-stu-id="67b73-113">Test a specific route.</span></span>

## <span data-ttu-id="67b73-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67b73-114">EXAMPLES</span></span>

### <span data-ttu-id="67b73-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67b73-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="67b73-116">Testare tutte le route con "DeviceMessages" di origine.</span><span class="sxs-lookup"><span data-stu-id="67b73-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="67b73-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="67b73-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="67b73-118">Testare un percorso specifico.</span><span class="sxs-lookup"><span data-stu-id="67b73-118">Test a specific route.</span></span>

### <span data-ttu-id="67b73-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="67b73-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="67b73-120">Testare un percorso specifico e visualizzare il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="67b73-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="67b73-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="67b73-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="67b73-122">Testare una route specifica con AppProperty e SystemProperty.</span><span class="sxs-lookup"><span data-stu-id="67b73-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="67b73-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67b73-123">PARAMETERS</span></span>

### <span data-ttu-id="67b73-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="67b73-124">-AppProperty</span></span>
<span data-ttu-id="67b73-125">Proprietà dell'app del messaggio di instrado</span><span class="sxs-lookup"><span data-stu-id="67b73-125">App properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-126">-Body</span><span class="sxs-lookup"><span data-stu-id="67b73-126">-Body</span></span>
<span data-ttu-id="67b73-127">Corpo del messaggio di route</span><span class="sxs-lookup"><span data-stu-id="67b73-127">Body of the route message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b73-128">-DefaultProfile</span></span>
<span data-ttu-id="67b73-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67b73-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67b73-130">-InputObject</span></span>
<span data-ttu-id="67b73-131">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="67b73-131">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-132">-Name</span><span class="sxs-lookup"><span data-stu-id="67b73-132">-Name</span></span>
<span data-ttu-id="67b73-133">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="67b73-133">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b73-134">-ResourceGroupName</span></span>
<span data-ttu-id="67b73-135">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="67b73-135">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67b73-136">-ResourceId</span></span>
<span data-ttu-id="67b73-137">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="67b73-137">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="67b73-138">-RouteName</span></span>
<span data-ttu-id="67b73-139">Nome del percorso</span><span class="sxs-lookup"><span data-stu-id="67b73-139">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="67b73-140">-ShowError</span></span>
<span data-ttu-id="67b73-141">Mostra errore dettagliato, se esistente</span><span class="sxs-lookup"><span data-stu-id="67b73-141">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-142">-Source</span><span class="sxs-lookup"><span data-stu-id="67b73-142">-Source</span></span>
<span data-ttu-id="67b73-143">Origine del percorso</span><span class="sxs-lookup"><span data-stu-id="67b73-143">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="67b73-144">-SystemProperty</span></span>
<span data-ttu-id="67b73-145">Proprietà di sistema del messaggio di route</span><span class="sxs-lookup"><span data-stu-id="67b73-145">System properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67b73-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b73-146">CommonParameters</span></span>
<span data-ttu-id="67b73-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b73-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b73-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b73-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b73-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="67b73-149">INPUTS</span></span>

### <span data-ttu-id="67b73-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="67b73-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="67b73-151">System.String</span><span class="sxs-lookup"><span data-stu-id="67b73-151">System.String</span></span>

## <span data-ttu-id="67b73-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67b73-152">OUTPUTS</span></span>

### <span data-ttu-id="67b73-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="67b73-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="67b73-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="67b73-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="67b73-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="67b73-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="67b73-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="67b73-156">NOTES</span></span>

## <span data-ttu-id="67b73-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67b73-157">RELATED LINKS</span></span>
