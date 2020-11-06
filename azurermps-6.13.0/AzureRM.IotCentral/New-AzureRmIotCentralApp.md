---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/new-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
ms.openlocfilehash: d0bb10324c1a97b6228a26a7ab079edb4845d48a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521852"
---
# <span data-ttu-id="40524-101">New-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="40524-101">New-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="40524-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40524-102">SYNOPSIS</span></span>
<span data-ttu-id="40524-103">Crea una nuova applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="40524-103">Creates a new IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40524-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40524-104">SYNTAX</span></span>

```
New-AzureRmIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40524-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40524-105">DESCRIPTION</span></span>
<span data-ttu-id="40524-106">Crea una nuova applicazione centrale di un sacco con le proprietà e i metadati forniti.</span><span class="sxs-lookup"><span data-stu-id="40524-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="40524-107">Per un'introduzione al centro informazioni, vedere https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="40524-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="40524-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40524-108">EXAMPLES</span></span>

### <span data-ttu-id="40524-109">L'esempio 1 crea un'applicazione centrale semplice.</span><span class="sxs-lookup"><span data-stu-id="40524-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="40524-110">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="40524-110">Example Output:</span></span>

<span data-ttu-id="40524-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName subdomain: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx</span><span class="sxs-lookup"><span data-stu-id="40524-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="40524-112">Creare un'applicazione centrale molto nel livello di prezzo standard S1 nell'area del gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="40524-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="40524-113">Esempio 2 creare un'applicazione centrale semplice.</span><span class="sxs-lookup"><span data-stu-id="40524-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="40524-114">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="40524-114">Example Output:</span></span>

<span data-ttu-id="40524-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName nome: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom nome visualizzato subdomain: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40524-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="40524-116">Creare un'applicazione centrale molto con il livello di prezzo standard S1 nell'area "westus", con un nome visualizzato personalizzato, basato sul modello predefinito di IOTC.</span><span class="sxs-lookup"><span data-stu-id="40524-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="40524-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40524-117">PARAMETERS</span></span>

### <span data-ttu-id="40524-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40524-118">-AsJob</span></span>
<span data-ttu-id="40524-119">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="40524-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40524-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40524-120">-DefaultProfile</span></span>
<span data-ttu-id="40524-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40524-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40524-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="40524-122">-DisplayName</span></span>
<span data-ttu-id="40524-123">Nome visualizzato personalizzato per l'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="40524-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="40524-124">L'impostazione predefinita è nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="40524-124">Default is resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40524-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="40524-125">-Location</span></span>
<span data-ttu-id="40524-126">Posizione dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="40524-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="40524-127">Il valore predefinito è la posizione del gruppo di risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="40524-127">Default is the location of target resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40524-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="40524-128">-Name</span></span>
<span data-ttu-id="40524-129">Nome della risorsa dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="40524-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40524-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40524-130">-ResourceGroupName</span></span>
<span data-ttu-id="40524-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40524-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40524-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="40524-132">-Sku</span></span>
<span data-ttu-id="40524-133">Livello dei prezzi per le applicazioni centrali di un sacco.</span><span class="sxs-lookup"><span data-stu-id="40524-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="40524-134">Il valore predefinito è S1.</span><span class="sxs-lookup"><span data-stu-id="40524-134">Default value is S1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40524-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="40524-135">-Subdomain</span></span>
<span data-ttu-id="40524-136">Sottodominio per l'URL centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="40524-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="40524-137">Ogni applicazione deve avere un sottodominio univoco.</span><span class="sxs-lookup"><span data-stu-id="40524-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40524-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="40524-138">-Tag</span></span>
<span data-ttu-id="40524-139">Tag delle risorse dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="40524-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40524-140">-Modello</span><span class="sxs-lookup"><span data-stu-id="40524-140">-Template</span></span>
<span data-ttu-id="40524-141">Nome del modello di applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="40524-141">IoT Central application template name.</span></span>
<span data-ttu-id="40524-142">L'impostazione predefinita è un'applicazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="40524-142">Default is a custom application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40524-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40524-143">-Confirm</span></span>
<span data-ttu-id="40524-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40524-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40524-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40524-145">-WhatIf</span></span>
<span data-ttu-id="40524-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40524-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40524-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40524-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40524-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40524-148">CommonParameters</span></span>
<span data-ttu-id="40524-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40524-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40524-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40524-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40524-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40524-151">INPUTS</span></span>

### <span data-ttu-id="40524-152">System. String</span><span class="sxs-lookup"><span data-stu-id="40524-152">System.String</span></span>
### <span data-ttu-id="40524-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="40524-153">System.Collections.Hashtable</span></span>
## <span data-ttu-id="40524-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40524-154">OUTPUTS</span></span>

### <span data-ttu-id="40524-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="40524-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="40524-156">Note</span><span class="sxs-lookup"><span data-stu-id="40524-156">NOTES</span></span>

## <span data-ttu-id="40524-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40524-157">RELATED LINKS</span></span>
