---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 17ccb6e41e826ffd6b522c353ff51cf360b5af0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961325"
---
# <span data-ttu-id="a4ab6-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a4ab6-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="a4ab6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="a4ab6-103">Rimuove i criteri di replica degli oggetti specificati da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="a4ab6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4ab6-104">SYNTAX</span></span>

### <span data-ttu-id="a4ab6-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4ab6-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4ab6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a4ab6-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4ab6-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="a4ab6-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4ab6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4ab6-108">DESCRIPTION</span></span>
<span data-ttu-id="a4ab6-109">Il cmdlet **Remove-AzStorageObjectReplicationPolicy** rimuove il criterio di replica degli oggetti specificato da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="a4ab6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4ab6-110">EXAMPLES</span></span>

### <span data-ttu-id="a4ab6-111">Esempio 1: Rimuovere un criterio di replica degli oggetti con policyId specifico da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="a4ab6-112">Questo comando rimuove un criterio di replica degli oggetti con policyId specifico da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="a4ab6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4ab6-113">PARAMETERS</span></span>

### <span data-ttu-id="a4ab6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4ab6-114">-DefaultProfile</span></span>
<span data-ttu-id="a4ab6-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4ab6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4ab6-116">-InputObject</span></span>
<span data-ttu-id="a4ab6-117">Oggetto Criteri di replica degli oggetti da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-117">Object Replication Policy object to Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ab6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4ab6-118">-PassThru</span></span>
<span data-ttu-id="a4ab6-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a4ab6-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a4ab6-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="a4ab6-120">-PolicyId</span></span>
<span data-ttu-id="a4ab6-121">ID dei criteri di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-121">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ab6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4ab6-122">-ResourceGroupName</span></span>
<span data-ttu-id="a4ab6-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ab6-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a4ab6-124">-StorageAccount</span></span>
<span data-ttu-id="a4ab6-125">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a4ab6-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4ab6-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a4ab6-126">-StorageAccountName</span></span>
<span data-ttu-id="a4ab6-127">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4ab6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4ab6-128">-Confirm</span></span>
<span data-ttu-id="a4ab6-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4ab6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4ab6-130">-WhatIf</span></span>
<span data-ttu-id="a4ab6-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4ab6-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4ab6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4ab6-133">CommonParameters</span></span>
<span data-ttu-id="a4ab6-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4ab6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4ab6-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4ab6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4ab6-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4ab6-136">INPUTS</span></span>

### <span data-ttu-id="a4ab6-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a4ab6-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a4ab6-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a4ab6-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="a4ab6-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4ab6-139">OUTPUTS</span></span>

### <span data-ttu-id="a4ab6-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4ab6-140">System.Boolean</span></span>

## <span data-ttu-id="a4ab6-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4ab6-141">NOTES</span></span>

## <span data-ttu-id="a4ab6-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4ab6-142">RELATED LINKS</span></span>
