---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203909"
---
# <span data-ttu-id="3236b-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="3236b-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="3236b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3236b-102">SYNOPSIS</span></span>
<span data-ttu-id="3236b-103">Ottiene le proprietà per una o più applicazioni ioT Central.</span><span class="sxs-lookup"><span data-stu-id="3236b-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="3236b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3236b-104">SYNTAX</span></span>

### <span data-ttu-id="3236b-105">ListIotCentralAppsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3236b-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3236b-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="3236b-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3236b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3236b-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3236b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3236b-108">DESCRIPTION</span></span>
<span data-ttu-id="3236b-109">Ottiene i metadati per una specifica applicazione centrale IoT o per tutte le applicazioni in un gruppo di risorse o una sottoscrizione, a seconda del set di parametri.</span><span class="sxs-lookup"><span data-stu-id="3236b-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="3236b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3236b-110">EXAMPLES</span></span>

### <span data-ttu-id="3236b-111">Esempio 1: ottenere specifiche applicazioni ioT central.</span><span class="sxs-lookup"><span data-stu-id="3236b-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="3236b-112">Recupera i metadati per l'applicazione centrale IoT specificata.</span><span class="sxs-lookup"><span data-stu-id="3236b-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="3236b-113">Output di esempio:</span><span class="sxs-lookup"><span data-stu-id="3236b-113">Example Output:</span></span>

<span data-ttu-id="3236b-114">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU: Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3236b-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="3236b-115">Esempio 2: Ottenere applicazioni ioT central in abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3236b-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="3236b-116">Recupera i metadati per tutte le applicazioni di IoT Central nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="3236b-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="3236b-117">Output di esempio:</span><span class="sxs-lookup"><span data-stu-id="3236b-117">Example Output:</span></span>

<span data-ttu-id="3236b-118">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU: Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3236b-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="3236b-119">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name : MyAppResourceName2 Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} Sku : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="3236b-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="3236b-120">Esempio 3 Ottieni applicazioni centrali IoT nel gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3236b-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="3236b-121">Ottiene i metadati per tutte le applicazioni ioT central nel gruppo di risorse fornito.</span><span class="sxs-lookup"><span data-stu-id="3236b-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="3236b-122">Output di esempio:</span><span class="sxs-lookup"><span data-stu-id="3236b-122">Example Output:</span></span>

<span data-ttu-id="3236b-123">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU: Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppskuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3236b-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="3236b-124">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 Name : MyAppResourceName2 Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX RESOURCEGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3236b-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="3236b-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3236b-125">PARAMETERS</span></span>

### <span data-ttu-id="3236b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3236b-126">-DefaultProfile</span></span>
<span data-ttu-id="3236b-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3236b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3236b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3236b-128">-Name</span></span>
<span data-ttu-id="3236b-129">Nome della risorsa applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="3236b-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3236b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3236b-130">-ResourceGroupName</span></span>
<span data-ttu-id="3236b-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3236b-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3236b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3236b-132">-ResourceId</span></span>
<span data-ttu-id="3236b-133">ID risorsa applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="3236b-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3236b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3236b-134">CommonParameters</span></span>
<span data-ttu-id="3236b-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3236b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3236b-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3236b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3236b-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="3236b-137">INPUTS</span></span>

### <span data-ttu-id="3236b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3236b-138">System.String</span></span>

## <span data-ttu-id="3236b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3236b-139">OUTPUTS</span></span>

### <span data-ttu-id="3236b-140">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="3236b-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="3236b-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="3236b-141">NOTES</span></span>

## <span data-ttu-id="3236b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3236b-142">RELATED LINKS</span></span>
