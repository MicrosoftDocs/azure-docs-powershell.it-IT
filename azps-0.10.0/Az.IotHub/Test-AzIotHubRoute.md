---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: 3d5252f30d8d4393d84f77e1ae1076c9c8054d91
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863070"
---
# <span data-ttu-id="6db71-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="6db71-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="6db71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6db71-102">SYNOPSIS</span></span>
<span data-ttu-id="6db71-103">Testare le route in hub molto</span><span class="sxs-lookup"><span data-stu-id="6db71-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="6db71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6db71-104">SYNTAX</span></span>

### <span data-ttu-id="6db71-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6db71-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6db71-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="6db71-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6db71-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="6db71-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6db71-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="6db71-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6db71-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="6db71-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6db71-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="6db71-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6db71-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="6db71-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6db71-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6db71-112">DESCRIPTION</span></span>
<span data-ttu-id="6db71-113">Testare una route specifica.</span><span class="sxs-lookup"><span data-stu-id="6db71-113">Test a specific route.</span></span>

## <span data-ttu-id="6db71-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6db71-114">EXAMPLES</span></span>

### <span data-ttu-id="6db71-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6db71-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="6db71-116">Testare tutte le route con l'origine "DeviceMessages".</span><span class="sxs-lookup"><span data-stu-id="6db71-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="6db71-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6db71-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="6db71-118">Testare una route specifica.</span><span class="sxs-lookup"><span data-stu-id="6db71-118">Test a specific route.</span></span>

### <span data-ttu-id="6db71-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6db71-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="6db71-120">Testare una route specifica e visualizzare il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="6db71-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="6db71-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6db71-121">PARAMETERS</span></span>

### <span data-ttu-id="6db71-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="6db71-122">-AppProperty</span></span>
<span data-ttu-id="6db71-123">Proprietà delle app del messaggio Route</span><span class="sxs-lookup"><span data-stu-id="6db71-123">App properties of the route message</span></span>

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

### <span data-ttu-id="6db71-124">-Body</span><span class="sxs-lookup"><span data-stu-id="6db71-124">-Body</span></span>
<span data-ttu-id="6db71-125">Corpo del messaggio Route</span><span class="sxs-lookup"><span data-stu-id="6db71-125">Body of the route message</span></span>

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

### <span data-ttu-id="6db71-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db71-126">-DefaultProfile</span></span>
<span data-ttu-id="6db71-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6db71-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6db71-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6db71-128">-InputObject</span></span>
<span data-ttu-id="6db71-129">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="6db71-129">IotHub Object</span></span>

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

### <span data-ttu-id="6db71-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="6db71-130">-Name</span></span>
<span data-ttu-id="6db71-131">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="6db71-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6db71-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db71-132">-ResourceGroupName</span></span>
<span data-ttu-id="6db71-133">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6db71-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6db71-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6db71-134">-ResourceId</span></span>
<span data-ttu-id="6db71-135">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="6db71-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6db71-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="6db71-136">-RouteName</span></span>
<span data-ttu-id="6db71-137">Nome della route</span><span class="sxs-lookup"><span data-stu-id="6db71-137">Name of the Route</span></span>

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

### <span data-ttu-id="6db71-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="6db71-138">-ShowError</span></span>
<span data-ttu-id="6db71-139">Mostra errore dettagliato, se esistente</span><span class="sxs-lookup"><span data-stu-id="6db71-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="6db71-140">-Origine</span><span class="sxs-lookup"><span data-stu-id="6db71-140">-Source</span></span>
<span data-ttu-id="6db71-141">Origine della route</span><span class="sxs-lookup"><span data-stu-id="6db71-141">Source of the route</span></span>

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

### <span data-ttu-id="6db71-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="6db71-142">-SystemProperty</span></span>
<span data-ttu-id="6db71-143">Proprietà di sistema del messaggio Route</span><span class="sxs-lookup"><span data-stu-id="6db71-143">System properties of the route message</span></span>

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

### <span data-ttu-id="6db71-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db71-144">CommonParameters</span></span>
<span data-ttu-id="6db71-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db71-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db71-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db71-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db71-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6db71-147">INPUTS</span></span>

### <span data-ttu-id="6db71-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6db71-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6db71-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6db71-149">System.String</span></span>

## <span data-ttu-id="6db71-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6db71-150">OUTPUTS</span></span>

### <span data-ttu-id="6db71-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="6db71-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="6db71-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError</span><span class="sxs-lookup"><span data-stu-id="6db71-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="6db71-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="6db71-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="6db71-154">Note</span><span class="sxs-lookup"><span data-stu-id="6db71-154">NOTES</span></span>

## <span data-ttu-id="6db71-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6db71-155">RELATED LINKS</span></span>
