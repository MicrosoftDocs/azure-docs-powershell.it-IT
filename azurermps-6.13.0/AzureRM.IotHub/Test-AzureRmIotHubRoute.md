---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/test-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Test-AzureRmIotHubRoute.md
ms.openlocfilehash: f51ba85215d252959b974a39ea864b1c98fce460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687843"
---
# <span data-ttu-id="acba6-101">Test-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="acba6-101">Test-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="acba6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="acba6-102">SYNOPSIS</span></span>
<span data-ttu-id="acba6-103">Testare le route in hub molto</span><span class="sxs-lookup"><span data-stu-id="acba6-103">Test routes in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acba6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acba6-104">SYNTAX</span></span>

### <span data-ttu-id="acba6-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="acba6-105">ResourceSet (Default)</span></span>
```
Test-AzureRmIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acba6-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="acba6-106">InputObjectTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acba6-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="acba6-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acba6-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="acba6-108">TestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acba6-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="acba6-109">TestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource>
 [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acba6-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="acba6-110">ResourceIdTestRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acba6-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="acba6-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzureRmIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acba6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acba6-112">DESCRIPTION</span></span>
<span data-ttu-id="acba6-113">Testare una route specifica.</span><span class="sxs-lookup"><span data-stu-id="acba6-113">Test a specific route.</span></span>

## <span data-ttu-id="acba6-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acba6-114">EXAMPLES</span></span>

### <span data-ttu-id="acba6-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="acba6-115">Example 1</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="acba6-116">Testare tutte le route con l'origine "DeviceMessges".</span><span class="sxs-lookup"><span data-stu-id="acba6-116">Test all route with source "DeviceMessges".</span></span>

### <span data-ttu-id="acba6-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="acba6-117">Example 2</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="acba6-118">Testare una route specifica.</span><span class="sxs-lookup"><span data-stu-id="acba6-118">Test a specific route.</span></span>

### <span data-ttu-id="acba6-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="acba6-119">Example 3</span></span>
```
PS C:\> Test-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="acba6-120">Testare una route specifica e visualizzare il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="acba6-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="acba6-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="acba6-121">PARAMETERS</span></span>

### <span data-ttu-id="acba6-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="acba6-122">-AppProperty</span></span>
<span data-ttu-id="acba6-123">Proprietà delle app del messaggio Route</span><span class="sxs-lookup"><span data-stu-id="acba6-123">App properties of the route message</span></span>

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

### <span data-ttu-id="acba6-124">-Body</span><span class="sxs-lookup"><span data-stu-id="acba6-124">-Body</span></span>
<span data-ttu-id="acba6-125">Corpo del messaggio Route</span><span class="sxs-lookup"><span data-stu-id="acba6-125">Body of the route message</span></span>

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

### <span data-ttu-id="acba6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acba6-126">-DefaultProfile</span></span>
<span data-ttu-id="acba6-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acba6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acba6-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acba6-128">-InputObject</span></span>
<span data-ttu-id="acba6-129">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="acba6-129">IotHub Object</span></span>

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

### <span data-ttu-id="acba6-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="acba6-130">-Name</span></span>
<span data-ttu-id="acba6-131">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="acba6-131">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="acba6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acba6-132">-ResourceGroupName</span></span>
<span data-ttu-id="acba6-133">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="acba6-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="acba6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acba6-134">-ResourceId</span></span>
<span data-ttu-id="acba6-135">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="acba6-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="acba6-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="acba6-136">-RouteName</span></span>
<span data-ttu-id="acba6-137">Nome della route</span><span class="sxs-lookup"><span data-stu-id="acba6-137">Name of the Route</span></span>

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

### <span data-ttu-id="acba6-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="acba6-138">-ShowError</span></span>
<span data-ttu-id="acba6-139">Mostra errore dettagliato, se esistente</span><span class="sxs-lookup"><span data-stu-id="acba6-139">Show detailed error, if exist</span></span>

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

### <span data-ttu-id="acba6-140">-Origine</span><span class="sxs-lookup"><span data-stu-id="acba6-140">-Source</span></span>
<span data-ttu-id="acba6-141">Origine della route</span><span class="sxs-lookup"><span data-stu-id="acba6-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acba6-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="acba6-142">-SystemProperty</span></span>
<span data-ttu-id="acba6-143">Proprietà di sistema del messaggio Route</span><span class="sxs-lookup"><span data-stu-id="acba6-143">System properties of the route message</span></span>

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

### <span data-ttu-id="acba6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acba6-144">CommonParameters</span></span>
<span data-ttu-id="acba6-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acba6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acba6-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acba6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acba6-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="acba6-147">INPUTS</span></span>

### <span data-ttu-id="acba6-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="acba6-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="acba6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="acba6-149">System.String</span></span>

## <span data-ttu-id="acba6-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acba6-150">OUTPUTS</span></span>

### <span data-ttu-id="acba6-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSTestRouteResult</span><span class="sxs-lookup"><span data-stu-id="acba6-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>
<span data-ttu-id="acba6-152">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteCompilationError System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="acba6-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="acba6-153">Note</span><span class="sxs-lookup"><span data-stu-id="acba6-153">NOTES</span></span>

## <span data-ttu-id="acba6-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acba6-154">RELATED LINKS</span></span>
