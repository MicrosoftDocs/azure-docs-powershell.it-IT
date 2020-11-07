---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 636c40763c69a4c39ca0bbf8b15fe04fad318d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674263"
---
# <span data-ttu-id="93a74-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="93a74-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="93a74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93a74-102">SYNOPSIS</span></span>
<span data-ttu-id="93a74-103">Crea una nuova applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="93a74-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="93a74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93a74-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93a74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93a74-105">DESCRIPTION</span></span>
<span data-ttu-id="93a74-106">Crea una nuova applicazione centrale di un sacco con le proprietà e i metadati forniti.</span><span class="sxs-lookup"><span data-stu-id="93a74-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="93a74-107">Per un'introduzione al centro informazioni, vedere https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="93a74-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="93a74-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93a74-108">EXAMPLES</span></span>

### <span data-ttu-id="93a74-109">L'esempio 1 crea un'applicazione centrale semplice.</span><span class="sxs-lookup"><span data-stu-id="93a74-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="93a74-110">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="93a74-110">Example Output:</span></span>

<span data-ttu-id="93a74-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName subdomain: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx</span><span class="sxs-lookup"><span data-stu-id="93a74-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="93a74-112">Creare un'applicazione centrale molto nel livello di prezzo standard S1 nell'area del gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="93a74-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="93a74-113">Esempio 2 creare un'applicazione centrale semplice.</span><span class="sxs-lookup"><span data-stu-id="93a74-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="93a74-114">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="93a74-114">Example Output:</span></span>

<span data-ttu-id="93a74-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName nome: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My Custom nome visualizzato subdomain: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a74-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="93a74-116">Creare un'applicazione centrale molto con il livello di prezzo standard S1 nell'area "westus", con un nome visualizzato personalizzato, basato sul modello predefinito di IOTC.</span><span class="sxs-lookup"><span data-stu-id="93a74-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="93a74-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93a74-117">PARAMETERS</span></span>

### <span data-ttu-id="93a74-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93a74-118">-AsJob</span></span>
<span data-ttu-id="93a74-119">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="93a74-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a74-120">-DefaultProfile</span></span>
<span data-ttu-id="93a74-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93a74-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93a74-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="93a74-122">-DisplayName</span></span>
<span data-ttu-id="93a74-123">Nome visualizzato personalizzato per l'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="93a74-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="93a74-124">L'impostazione predefinita è nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="93a74-124">Default is resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="93a74-125">-Location</span></span>
<span data-ttu-id="93a74-126">Posizione dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="93a74-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="93a74-127">Il valore predefinito è la posizione del gruppo di risorse di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93a74-127">Default is the location of target resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="93a74-128">-Name</span></span>
<span data-ttu-id="93a74-129">Nome della risorsa dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="93a74-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93a74-130">-ResourceGroupName</span></span>
<span data-ttu-id="93a74-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93a74-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="93a74-132">-Sku</span></span>
<span data-ttu-id="93a74-133">Livello dei prezzi per le applicazioni centrali di un sacco.</span><span class="sxs-lookup"><span data-stu-id="93a74-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="93a74-134">Il valore predefinito è S1.</span><span class="sxs-lookup"><span data-stu-id="93a74-134">Default value is S1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="93a74-135">-Subdomain</span></span>
<span data-ttu-id="93a74-136">Sottodominio per l'URL centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="93a74-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="93a74-137">Ogni applicazione deve avere un sottodominio univoco.</span><span class="sxs-lookup"><span data-stu-id="93a74-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="93a74-138">-Tag</span></span>
<span data-ttu-id="93a74-139">Tag delle risorse dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="93a74-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-140">-Modello</span><span class="sxs-lookup"><span data-stu-id="93a74-140">-Template</span></span>
<span data-ttu-id="93a74-141">Nome del modello di applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="93a74-141">IoT Central application template name.</span></span>
<span data-ttu-id="93a74-142">L'impostazione predefinita è un'applicazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="93a74-142">Default is a custom application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="93a74-143">-Confirm</span></span>
<span data-ttu-id="93a74-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93a74-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93a74-145">-WhatIf</span></span>
<span data-ttu-id="93a74-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93a74-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93a74-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93a74-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93a74-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a74-148">CommonParameters</span></span>
<span data-ttu-id="93a74-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93a74-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a74-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93a74-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a74-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93a74-151">INPUTS</span></span>

### <span data-ttu-id="93a74-152">System. String</span><span class="sxs-lookup"><span data-stu-id="93a74-152">System.String</span></span>

### <span data-ttu-id="93a74-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="93a74-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="93a74-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93a74-154">OUTPUTS</span></span>

### <span data-ttu-id="93a74-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="93a74-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="93a74-156">Note</span><span class="sxs-lookup"><span data-stu-id="93a74-156">NOTES</span></span>

## <span data-ttu-id="93a74-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93a74-157">RELATED LINKS</span></span>
