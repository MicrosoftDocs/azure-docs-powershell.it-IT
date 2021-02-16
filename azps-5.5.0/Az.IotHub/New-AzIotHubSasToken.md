---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200095"
---
# <span data-ttu-id="2ac47-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="2ac47-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="2ac47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac47-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac47-103">Generare un token di firma di accesso condiviso per un hub IoT, un dispositivo o un modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2ac47-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="2ac47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ac47-104">SYNTAX</span></span>

### <span data-ttu-id="2ac47-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ac47-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac47-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ac47-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ac47-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2ac47-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ac47-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2ac47-108">DESCRIPTION</span></span>
<span data-ttu-id="2ac47-109">Per i token di firma di accesso condiviso del dispositivo, il parametro dei criteri viene usato solo per accedere al Registro di sistema del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ac47-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="2ac47-110">Di conseguenza, i criteri devono avere accesso in lettura al Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2ac47-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="2ac47-111">Per i token dell'Hub IoT, il criterio fa parte della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="2ac47-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="2ac47-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ac47-112">EXAMPLES</span></span>

### <span data-ttu-id="2ac47-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ac47-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="2ac47-114">Generare un token di firma di accesso condiviso dell'Hub IoT usando il criterio iothubowner e la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="2ac47-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="2ac47-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2ac47-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="2ac47-116">Generare un token di firma di accesso condiviso dell'Hub IoT usando il criterio RegistryRead e la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="2ac47-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="2ac47-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2ac47-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="2ac47-118">Genera un token di firma di accesso condiviso del dispositivo usando i criteri iothubowner per accedere al Registro di sistema del dispositivo {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="2ac47-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="2ac47-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="2ac47-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="2ac47-120">Generare un token di firma di accesso condiviso del modulo usando i criteri iothubowner per accedere al Registro di sistema del dispositivo {iothub_name}.</span><span class="sxs-lookup"><span data-stu-id="2ac47-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="2ac47-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ac47-121">PARAMETERS</span></span>

### <span data-ttu-id="2ac47-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac47-122">-DefaultProfile</span></span>
<span data-ttu-id="2ac47-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac47-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ac47-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2ac47-124">-DeviceId</span></span>
<span data-ttu-id="2ac47-125">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2ac47-125">Target Device Id.</span></span>

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

### <span data-ttu-id="2ac47-126">-Durata</span><span class="sxs-lookup"><span data-stu-id="2ac47-126">-Duration</span></span>
<span data-ttu-id="2ac47-127">Scadenza futura (in secondi) del token da generare.</span><span class="sxs-lookup"><span data-stu-id="2ac47-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="2ac47-128">L'impostazione predefinita è 3600.</span><span class="sxs-lookup"><span data-stu-id="2ac47-128">Default is 3600.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac47-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac47-129">-InputObject</span></span>
<span data-ttu-id="2ac47-130">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="2ac47-130">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac47-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2ac47-131">-IotHubName</span></span>
<span data-ttu-id="2ac47-132">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="2ac47-132">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac47-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2ac47-133">-KeyName</span></span>
<span data-ttu-id="2ac47-134">Nome della chiave di accesso.</span><span class="sxs-lookup"><span data-stu-id="2ac47-134">Access key name.</span></span>

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

### <span data-ttu-id="2ac47-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2ac47-135">-KeyType</span></span>
<span data-ttu-id="2ac47-136">Tipo di tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="2ac47-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac47-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="2ac47-137">-ModuleId</span></span>
<span data-ttu-id="2ac47-138">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2ac47-138">Target Module Id.</span></span>

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

### <span data-ttu-id="2ac47-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac47-139">-ResourceGroupName</span></span>
<span data-ttu-id="2ac47-140">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2ac47-140">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac47-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac47-141">-ResourceId</span></span>
<span data-ttu-id="2ac47-142">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="2ac47-142">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac47-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ac47-143">-Confirm</span></span>
<span data-ttu-id="2ac47-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ac47-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ac47-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac47-145">-WhatIf</span></span>
<span data-ttu-id="2ac47-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ac47-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac47-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ac47-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ac47-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac47-148">CommonParameters</span></span>
<span data-ttu-id="2ac47-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac47-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac47-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac47-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac47-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="2ac47-151">INPUTS</span></span>

### <span data-ttu-id="2ac47-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2ac47-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2ac47-153">System.String</span><span class="sxs-lookup"><span data-stu-id="2ac47-153">System.String</span></span>

## <span data-ttu-id="2ac47-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ac47-154">OUTPUTS</span></span>

### <span data-ttu-id="2ac47-155">System.String</span><span class="sxs-lookup"><span data-stu-id="2ac47-155">System.String</span></span>

## <span data-ttu-id="2ac47-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="2ac47-156">NOTES</span></span>

## <span data-ttu-id="2ac47-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ac47-157">RELATED LINKS</span></span>
