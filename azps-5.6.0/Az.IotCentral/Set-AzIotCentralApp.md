---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: f99faf1ce7420212e87c894c8f5aadeb16578334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997960"
---
# <span data-ttu-id="7ca6c-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7ca6c-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="7ca6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ca6c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca6c-103">Aggiorna i metadati per un'applicazione centrale IoT.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="7ca6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ca6c-104">SYNTAX</span></span>

### <span data-ttu-id="7ca6c-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ca6c-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ca6c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca6c-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ca6c-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ca6c-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ca6c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7ca6c-108">DESCRIPTION</span></span>
<span data-ttu-id="7ca6c-109">Aggiornare i metadati per un'applicazione centrale IoT.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="7ca6c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ca6c-110">EXAMPLES</span></span>

### <span data-ttu-id="7ca6c-111">Esempio 1: aggiornare il nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="7ca6c-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="7ca6c-112">Aggiornare il nome visualizzato in un'applicazione centrale IoT esistente.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="7ca6c-113">Output di esempio:</span><span class="sxs-lookup"><span data-stu-id="7ca6c-113">Example Output:</span></span>

<span data-ttu-id="7ca6c-114">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXX XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Nuovo sottodominio nome visualizzato personalizzato : Modello MyAppSubdomain : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca6c-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="7ca6c-115">Esempio 2: Aggiornare il sottodominio</span><span class="sxs-lookup"><span data-stu-id="7ca6c-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="7ca6c-116">Aggiornare il nome visualizzato in un'applicazione centrale IoT esistente.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="7ca6c-117">Output di esempio:</span><span class="sxs-lookup"><span data-stu-id="7ca6c-117">Example Output:</span></span>

<span data-ttu-id="7ca6c-118">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Sottodominio nome visualizzato : nuovo sottodominio - Modello : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca6c-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="7ca6c-119">Esempio 3: Aggiornare le informazioni sulle SKU dell'app</span><span class="sxs-lookup"><span data-stu-id="7ca6c-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="7ca6c-120">Aggiornare la SKU in un'applicazione centrale IoT esistente.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="7ca6c-121">Output di esempio:</span><span class="sxs-lookup"><span data-stu-id="7ca6c-121">Example Output:</span></span>

<span data-ttu-id="7ca6c-122">ResourceId: /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName : Sottodominio Nome visualizzato : Modello MyAppSubdomain iotc-default@1.0.0 : SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca6c-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="7ca6c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ca6c-123">PARAMETERS</span></span>

### <span data-ttu-id="7ca6c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ca6c-124">-AsJob</span></span>
<span data-ttu-id="7ca6c-125">Eseguire il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="7ca6c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca6c-126">-DefaultProfile</span></span>
<span data-ttu-id="7ca6c-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ca6c-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7ca6c-128">-DisplayName</span></span>
<span data-ttu-id="7ca6c-129">Nome visualizzato personalizzato dell'applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="7ca6c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ca6c-130">-InputObject</span></span>
<span data-ttu-id="7ca6c-131">Oggetto di input Iot Central Application.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ca6c-132">-Name</span><span class="sxs-lookup"><span data-stu-id="7ca6c-132">-Name</span></span>
<span data-ttu-id="7ca6c-133">Nome della risorsa applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="7ca6c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca6c-134">-ResourceGroupName</span></span>
<span data-ttu-id="7ca6c-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="7ca6c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ca6c-136">-ResourceId</span></span>
<span data-ttu-id="7ca6c-137">ID risorsa applicazione centrale Iot.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="7ca6c-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="7ca6c-138">-Sku</span></span>
<span data-ttu-id="7ca6c-139">Pricing tier per le applicazioni IoT Central.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="7ca6c-140">Il valore predefinito è ST2.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="7ca6c-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="7ca6c-141">-Subdomain</span></span>
<span data-ttu-id="7ca6c-142">Sottodominio dell'applicazione centrale IoT.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="7ca6c-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="7ca6c-143">-Tag</span></span>
<span data-ttu-id="7ca6c-144">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-144">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="7ca6c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ca6c-145">-Confirm</span></span>
<span data-ttu-id="7ca6c-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca6c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca6c-147">-WhatIf</span></span>
<span data-ttu-id="7ca6c-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ca6c-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca6c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca6c-150">CommonParameters</span></span>
<span data-ttu-id="7ca6c-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca6c-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7ca6c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca6c-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="7ca6c-153">INPUTS</span></span>

### <span data-ttu-id="7ca6c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="7ca6c-154">System.String</span></span>

### <span data-ttu-id="7ca6c-155">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7ca6c-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="7ca6c-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ca6c-156">OUTPUTS</span></span>

### <span data-ttu-id="7ca6c-157">Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="7ca6c-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="7ca6c-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="7ca6c-158">NOTES</span></span>

## <span data-ttu-id="7ca6c-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ca6c-159">RELATED LINKS</span></span>
