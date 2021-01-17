---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 173e84e3587a6844896791ef38a185db522d4e4b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386438"
---
# <span data-ttu-id="c67ee-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="c67ee-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="c67ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c67ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c67ee-103">Testare le route in hub molto</span><span class="sxs-lookup"><span data-stu-id="c67ee-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="c67ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c67ee-104">SYNTAX</span></span>

### <span data-ttu-id="c67ee-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c67ee-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c67ee-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="c67ee-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c67ee-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="c67ee-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c67ee-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="c67ee-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c67ee-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="c67ee-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c67ee-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="c67ee-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c67ee-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="c67ee-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c67ee-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c67ee-112">DESCRIPTION</span></span>
<span data-ttu-id="c67ee-113">Testare una route specifica.</span><span class="sxs-lookup"><span data-stu-id="c67ee-113">Test a specific route.</span></span>

## <span data-ttu-id="c67ee-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c67ee-114">EXAMPLES</span></span>

### <span data-ttu-id="c67ee-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c67ee-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="c67ee-116">Testare tutte le route con l'origine "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="c67ee-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="c67ee-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c67ee-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="c67ee-118">Testare una route specifica.</span><span class="sxs-lookup"><span data-stu-id="c67ee-118">Test a specific route.</span></span>

### <span data-ttu-id="c67ee-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c67ee-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="c67ee-120">Testare una route specifica e visualizzare il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c67ee-120">Test a specific route and showing the reason of failure.</span></span>

### <span data-ttu-id="c67ee-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="c67ee-121">Example 4</span></span>
```
PS C:\> $ap = @{}
PS C:\> $ap.add("key0","value0")
PS C:\> $sp = @{}
PS C:\> $sp.add("key1", "value1")
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -AppProperty $ap -SystemProperty $sp

Result : true
```

<span data-ttu-id="c67ee-122">Testare una route specifica con AppProperty e SystemProperty.</span><span class="sxs-lookup"><span data-stu-id="c67ee-122">Test a specific route with AppProperty and SystemProperty.</span></span>

## <span data-ttu-id="c67ee-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c67ee-123">PARAMETERS</span></span>

### <span data-ttu-id="c67ee-124">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="c67ee-124">-AppProperty</span></span>
<span data-ttu-id="c67ee-125">Proprietà delle app del messaggio Route</span><span class="sxs-lookup"><span data-stu-id="c67ee-125">App properties of the route message</span></span>

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

### <span data-ttu-id="c67ee-126">-Body</span><span class="sxs-lookup"><span data-stu-id="c67ee-126">-Body</span></span>
<span data-ttu-id="c67ee-127">Corpo del messaggio Route</span><span class="sxs-lookup"><span data-stu-id="c67ee-127">Body of the route message</span></span>

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

### <span data-ttu-id="c67ee-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c67ee-128">-DefaultProfile</span></span>
<span data-ttu-id="c67ee-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c67ee-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c67ee-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c67ee-130">-InputObject</span></span>
<span data-ttu-id="c67ee-131">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="c67ee-131">IotHub Object</span></span>

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

### <span data-ttu-id="c67ee-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="c67ee-132">-Name</span></span>
<span data-ttu-id="c67ee-133">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="c67ee-133">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c67ee-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c67ee-134">-ResourceGroupName</span></span>
<span data-ttu-id="c67ee-135">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c67ee-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c67ee-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c67ee-136">-ResourceId</span></span>
<span data-ttu-id="c67ee-137">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="c67ee-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c67ee-138">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c67ee-138">-RouteName</span></span>
<span data-ttu-id="c67ee-139">Nome della route</span><span class="sxs-lookup"><span data-stu-id="c67ee-139">Name of the Route</span></span>

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

### <span data-ttu-id="c67ee-140">-ShowError</span><span class="sxs-lookup"><span data-stu-id="c67ee-140">-ShowError</span></span>
<span data-ttu-id="c67ee-141">Mostra errore dettagliato, se esistente</span><span class="sxs-lookup"><span data-stu-id="c67ee-141">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="c67ee-142">-Origine</span><span class="sxs-lookup"><span data-stu-id="c67ee-142">-Source</span></span>
<span data-ttu-id="c67ee-143">Origine della route</span><span class="sxs-lookup"><span data-stu-id="c67ee-143">Source of the route</span></span>

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

### <span data-ttu-id="c67ee-144">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="c67ee-144">-SystemProperty</span></span>
<span data-ttu-id="c67ee-145">Proprietà di sistema del messaggio Route</span><span class="sxs-lookup"><span data-stu-id="c67ee-145">System properties of the route message</span></span>

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

### <span data-ttu-id="c67ee-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c67ee-146">CommonParameters</span></span>
<span data-ttu-id="c67ee-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c67ee-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c67ee-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c67ee-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c67ee-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c67ee-149">INPUTS</span></span>

### <span data-ttu-id="c67ee-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c67ee-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c67ee-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c67ee-151">System.String</span></span>

## <span data-ttu-id="c67ee-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c67ee-152">OUTPUTS</span></span>

### <span data-ttu-id="c67ee-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="c67ee-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="c67ee-154">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="c67ee-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="c67ee-155">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="c67ee-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="c67ee-156">Note</span><span class="sxs-lookup"><span data-stu-id="c67ee-156">NOTES</span></span>

## <span data-ttu-id="c67ee-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c67ee-157">RELATED LINKS</span></span>
