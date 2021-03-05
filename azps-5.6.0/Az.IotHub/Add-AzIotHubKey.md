---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: fe964ba2672c67fc9bb5e47e7b7a16d4fdd49471
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997848"
---
# <span data-ttu-id="e39f7-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e39f7-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="e39f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e39f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e39f7-103">Crea una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="e39f7-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="e39f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e39f7-104">SYNTAX</span></span>

### <span data-ttu-id="e39f7-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e39f7-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e39f7-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e39f7-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e39f7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e39f7-107">DESCRIPTION</span></span>
<span data-ttu-id="e39f7-108">Crea una chiave per i dati di IotHub forniti.</span><span class="sxs-lookup"><span data-stu-id="e39f7-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="e39f7-109">KeyNames non è univoco e deve essere gestito con attenzione.</span><span class="sxs-lookup"><span data-stu-id="e39f7-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="e39f7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e39f7-110">EXAMPLES</span></span>

### <span data-ttu-id="e39f7-111">Esempio 1: Aggiungere una chiave a un iotHub</span><span class="sxs-lookup"><span data-stu-id="e39f7-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="e39f7-112">Crea una chiave denominata "mykey" per il file iothub "myiothub" con autorizzazioni RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="e39f7-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="e39f7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e39f7-113">PARAMETERS</span></span>

### <span data-ttu-id="e39f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e39f7-114">-DefaultProfile</span></span>
<span data-ttu-id="e39f7-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e39f7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e39f7-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="e39f7-116">-HubId</span></span>
<span data-ttu-id="e39f7-117">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="e39f7-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e39f7-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e39f7-118">-KeyName</span></span>
<span data-ttu-id="e39f7-119">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="e39f7-119">Name of the Key</span></span>

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

### <span data-ttu-id="e39f7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e39f7-120">-Name</span></span>
<span data-ttu-id="e39f7-121">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="e39f7-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e39f7-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e39f7-122">-PrimaryKey</span></span>
<span data-ttu-id="e39f7-123">Chiave primaria</span><span class="sxs-lookup"><span data-stu-id="e39f7-123">The primary key</span></span>

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

### <span data-ttu-id="e39f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e39f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="e39f7-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e39f7-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e39f7-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="e39f7-126">-Rights</span></span>
<span data-ttu-id="e39f7-127">Autorizzazioni per questo IOTHub</span><span class="sxs-lookup"><span data-stu-id="e39f7-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39f7-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="e39f7-128">-SecondaryKey</span></span>
<span data-ttu-id="e39f7-129">La chiave secondaria</span><span class="sxs-lookup"><span data-stu-id="e39f7-129">The Secondary Key</span></span>

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

### <span data-ttu-id="e39f7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e39f7-130">-Confirm</span></span>
<span data-ttu-id="e39f7-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e39f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e39f7-132">-WhatIf</span></span>
<span data-ttu-id="e39f7-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e39f7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e39f7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e39f7-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39f7-135">CommonParameters</span></span>
<span data-ttu-id="e39f7-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e39f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39f7-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e39f7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39f7-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="e39f7-138">INPUTS</span></span>

### <span data-ttu-id="e39f7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e39f7-139">System.String</span></span>

## <span data-ttu-id="e39f7-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e39f7-140">OUTPUTS</span></span>

### <span data-ttu-id="e39f7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e39f7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e39f7-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="e39f7-142">NOTES</span></span>

## <span data-ttu-id="e39f7-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e39f7-143">RELATED LINKS</span></span>
