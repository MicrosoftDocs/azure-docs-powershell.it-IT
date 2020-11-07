---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 0cac398a77c6d26ed9454b7345ce1bb8fde5b965
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864317"
---
# <span data-ttu-id="d6a86-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d6a86-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="d6a86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6a86-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a86-103">Ottiene le proprietà per una o più applicazioni centrali di un sacco.</span><span class="sxs-lookup"><span data-stu-id="d6a86-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="d6a86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6a86-104">SYNTAX</span></span>

### <span data-ttu-id="d6a86-105">ListIotCentralAppsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6a86-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6a86-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6a86-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6a86-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6a86-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6a86-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6a86-108">DESCRIPTION</span></span>
<span data-ttu-id="d6a86-109">Ottiene i metadati per un'applicazione centrale molto specifica o per tutte le applicazioni in un gruppo o un abbonamento a una risorsa, a seconda del set di parametri.</span><span class="sxs-lookup"><span data-stu-id="d6a86-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="d6a86-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6a86-110">EXAMPLES</span></span>

### <span data-ttu-id="d6a86-111">Esempio 1 ottenere un'applicazione centrale molto specifica.</span><span class="sxs-lookup"><span data-stu-id="d6a86-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="d6a86-112">Ottiene i metadati per l'applicazione centrale di un sacco specificata.</span><span class="sxs-lookup"><span data-stu-id="d6a86-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="d6a86-113">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="d6a86-113">Example Output:</span></span>

<span data-ttu-id="d6a86-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/IoTApps location: westus Tag: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom nome visualizzato subdomain: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx</span><span class="sxs-lookup"><span data-stu-id="d6a86-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="d6a86-115">Esempio 2 ottenere le applicazioni centrali di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d6a86-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="d6a86-116">Ottiene i metadati per tutte le applicazioni centrali di tutti gli altri nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d6a86-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="d6a86-117">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="d6a86-117">Example Output:</span></span>

<span data-ttu-id="d6a86-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/IoTApps location: westus Tag: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom nome visualizzato subdomain: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx</span><span class="sxs-lookup"><span data-stu-id="d6a86-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="d6a86-119">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 nome: MyAppResourceName2 tipo: Microsoft. IoTCentral/IoTApps località: westus Tag: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom nome visualizzato 2 sottodominio: MyAppSubdomain2 modello: SubscriptionID iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="d6a86-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="d6a86-120">Esempio 3 ottenere le applicazioni centrali di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6a86-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="d6a86-121">Ottiene i metadati per tutte le applicazioni centrali di tutti gli altri nel gruppo di risorse fornito.</span><span class="sxs-lookup"><span data-stu-id="d6a86-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="d6a86-122">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="d6a86-122">Example Output:</span></span>

<span data-ttu-id="d6a86-123">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/IoTApps location: westus Tag: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom nome visualizzato subdomain: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx</span><span class="sxs-lookup"><span data-stu-id="d6a86-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="d6a86-124">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 nome: MyAppResourceName2 tipo: Microsoft. IoTCentral/IoTApps località: westus Tag: {[Key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom nome visualizzato 2 sottodominio: MyAppSubdomain2 modello: SubscriptionID iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a86-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="d6a86-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6a86-125">PARAMETERS</span></span>

### <span data-ttu-id="d6a86-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a86-126">-DefaultProfile</span></span>
<span data-ttu-id="d6a86-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a86-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6a86-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6a86-128">-Name</span></span>
<span data-ttu-id="d6a86-129">Nome della risorsa dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="d6a86-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="d6a86-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a86-130">-ResourceGroupName</span></span>
<span data-ttu-id="d6a86-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6a86-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="d6a86-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6a86-132">-ResourceId</span></span>
<span data-ttu-id="d6a86-133">ID risorsa centrale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d6a86-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="d6a86-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a86-134">CommonParameters</span></span>
<span data-ttu-id="d6a86-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a86-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a86-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a86-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a86-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6a86-137">INPUTS</span></span>

### <span data-ttu-id="d6a86-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d6a86-138">System.String</span></span>

## <span data-ttu-id="d6a86-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6a86-139">OUTPUTS</span></span>

### <span data-ttu-id="d6a86-140">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="d6a86-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="d6a86-141">Note</span><span class="sxs-lookup"><span data-stu-id="d6a86-141">NOTES</span></span>

## <span data-ttu-id="d6a86-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6a86-142">RELATED LINKS</span></span>
