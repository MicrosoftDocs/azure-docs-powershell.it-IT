---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: d9a6936dec16f1723c0e74db7958093aca02ce97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983486"
---
# <span data-ttu-id="046c6-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="046c6-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="046c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="046c6-102">SYNOPSIS</span></span>
<span data-ttu-id="046c6-103">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="046c6-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="046c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="046c6-104">SYNTAX</span></span>

### <span data-ttu-id="046c6-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="046c6-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="046c6-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="046c6-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046c6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="046c6-107">DESCRIPTION</span></span>
<span data-ttu-id="046c6-108">Rimuove una chiave IotHub.</span><span class="sxs-lookup"><span data-stu-id="046c6-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="046c6-109">Se sono presenti più chiavi con lo stesso nome, la prima nell'elenco viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="046c6-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="046c6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="046c6-110">EXAMPLES</span></span>

### <span data-ttu-id="046c6-111">Esempio 1: Eliminare un iotHub</span><span class="sxs-lookup"><span data-stu-id="046c6-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="046c6-112">Rimuove la chiave denominata iothubowner1 da IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="046c6-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="046c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="046c6-113">PARAMETERS</span></span>

### <span data-ttu-id="046c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046c6-114">-DefaultProfile</span></span>
<span data-ttu-id="046c6-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="046c6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="046c6-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="046c6-116">-HubId</span></span>
<span data-ttu-id="046c6-117">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="046c6-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="046c6-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="046c6-118">-KeyName</span></span>
<span data-ttu-id="046c6-119">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="046c6-119">Name of the Key</span></span>

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

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046c6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="046c6-120">-Name</span></span>
<span data-ttu-id="046c6-121">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="046c6-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="046c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="046c6-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="046c6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="046c6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="046c6-124">-Confirm</span></span>
<span data-ttu-id="046c6-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="046c6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046c6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046c6-126">-WhatIf</span></span>
<span data-ttu-id="046c6-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="046c6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046c6-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="046c6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046c6-129">CommonParameters</span></span>
<span data-ttu-id="046c6-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="046c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046c6-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="046c6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046c6-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="046c6-132">INPUTS</span></span>

### <span data-ttu-id="046c6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="046c6-133">System.String</span></span>

## <span data-ttu-id="046c6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="046c6-134">OUTPUTS</span></span>

### <span data-ttu-id="046c6-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="046c6-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="046c6-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="046c6-136">NOTES</span></span>

## <span data-ttu-id="046c6-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="046c6-137">RELATED LINKS</span></span>
