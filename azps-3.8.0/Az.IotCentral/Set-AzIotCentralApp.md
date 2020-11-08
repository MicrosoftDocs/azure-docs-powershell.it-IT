---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: cea582481515f519e14df9f430dc1326e72a0877
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018445"
---
# <span data-ttu-id="afa88-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="afa88-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="afa88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="afa88-102">SYNOPSIS</span></span>
<span data-ttu-id="afa88-103">Aggiorna i metadati per un'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="afa88-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="afa88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afa88-104">SYNTAX</span></span>

### <span data-ttu-id="afa88-105">ResourceIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="afa88-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa88-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afa88-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afa88-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="afa88-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afa88-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afa88-108">DESCRIPTION</span></span>
<span data-ttu-id="afa88-109">Aggiornare i metadati per un'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="afa88-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="afa88-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afa88-110">EXAMPLES</span></span>

### <span data-ttu-id="afa88-111">Esempio 1 Aggiorna nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="afa88-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="afa88-112">Aggiornare il nome visualizzato in un'applicazione centrale di un sacco esistente.</span><span class="sxs-lookup"><span data-stu-id="afa88-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="afa88-113">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="afa88-113">Example Output:</span></span>

<span data-ttu-id="afa88-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName nome: MyAppResourceName tipo: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My New Custom nome visualizzato subdomain: MyAppSubdomain Template: SubscriptionID iotc-default@1.0.0 : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa88-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="afa88-115">Esempio 2 aggiornamento del sottodominio</span><span class="sxs-lookup"><span data-stu-id="afa88-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="afa88-116">Aggiornare il nome visualizzato in un'applicazione centrale di un sacco esistente.</span><span class="sxs-lookup"><span data-stu-id="afa88-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="afa88-117">Esempio di output:</span><span class="sxs-lookup"><span data-stu-id="afa88-117">Example Output:</span></span>

<span data-ttu-id="afa88-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/IoTApps location: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: display subdomain Name: New-subdomain Template: iotc-default@1.0.0 SubscriptionId: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa88-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="afa88-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="afa88-119">PARAMETERS</span></span>

### <span data-ttu-id="afa88-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afa88-120">-AsJob</span></span>
<span data-ttu-id="afa88-121">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="afa88-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="afa88-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa88-122">-DefaultProfile</span></span>
<span data-ttu-id="afa88-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afa88-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afa88-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="afa88-124">-DisplayName</span></span>
<span data-ttu-id="afa88-125">Nome visualizzato personalizzato dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="afa88-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="afa88-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afa88-126">-InputObject</span></span>
<span data-ttu-id="afa88-127">Oggetto di input dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="afa88-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="afa88-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="afa88-128">-Name</span></span>
<span data-ttu-id="afa88-129">Nome della risorsa dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="afa88-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="afa88-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa88-130">-ResourceGroupName</span></span>
<span data-ttu-id="afa88-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="afa88-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="afa88-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afa88-132">-ResourceId</span></span>
<span data-ttu-id="afa88-133">ID risorsa centrale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afa88-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="afa88-134">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="afa88-134">-Subdomain</span></span>
<span data-ttu-id="afa88-135">Sottodominio dell'applicazione centrale di un sacco.</span><span class="sxs-lookup"><span data-stu-id="afa88-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="afa88-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="afa88-136">-Tag</span></span>
<span data-ttu-id="afa88-137">Tag delle risorse dell'applicazione centrale.</span><span class="sxs-lookup"><span data-stu-id="afa88-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="afa88-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="afa88-138">-Confirm</span></span>
<span data-ttu-id="afa88-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afa88-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afa88-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afa88-140">-WhatIf</span></span>
<span data-ttu-id="afa88-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afa88-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afa88-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afa88-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afa88-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa88-143">CommonParameters</span></span>
<span data-ttu-id="afa88-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa88-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa88-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa88-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa88-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="afa88-146">INPUTS</span></span>

### <span data-ttu-id="afa88-147">System. String</span><span class="sxs-lookup"><span data-stu-id="afa88-147">System.String</span></span>

### <span data-ttu-id="afa88-148">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="afa88-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="afa88-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afa88-149">OUTPUTS</span></span>

### <span data-ttu-id="afa88-150">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="afa88-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="afa88-151">Note</span><span class="sxs-lookup"><span data-stu-id="afa88-151">NOTES</span></span>

## <span data-ttu-id="afa88-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afa88-152">RELATED LINKS</span></span>
