---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193762"
---
# <span data-ttu-id="24d80-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="24d80-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="24d80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24d80-102">SYNOPSIS</span></span>
<span data-ttu-id="24d80-103">Rimuove i criteri di replica degli oggetti specificati da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="24d80-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="24d80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24d80-104">SYNTAX</span></span>

### <span data-ttu-id="24d80-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24d80-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24d80-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="24d80-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24d80-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="24d80-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d80-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24d80-108">DESCRIPTION</span></span>
<span data-ttu-id="24d80-109">Il cmdlet **Remove-AzStorageObjectReplicationPolicy** rimuove i criteri di replica degli oggetti specificati da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="24d80-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="24d80-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24d80-110">EXAMPLES</span></span>

### <span data-ttu-id="24d80-111">Esempio 1: rimuovere un criterio di replica degli oggetti con policyId specifico da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="24d80-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="24d80-112">Questo comando rimuove un criterio di replica degli oggetti con policyId specifico da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="24d80-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="24d80-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24d80-113">PARAMETERS</span></span>

### <span data-ttu-id="24d80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d80-114">-DefaultProfile</span></span>
<span data-ttu-id="24d80-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24d80-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d80-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24d80-116">-InputObject</span></span>
<span data-ttu-id="24d80-117">Oggetto Criteri di replica degli oggetti da eliminare.</span><span class="sxs-lookup"><span data-stu-id="24d80-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="24d80-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24d80-118">-PassThru</span></span>
<span data-ttu-id="24d80-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="24d80-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="24d80-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="24d80-120">-PolicyId</span></span>
<span data-ttu-id="24d80-121">ID criterio di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="24d80-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="24d80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d80-122">-ResourceGroupName</span></span>
<span data-ttu-id="24d80-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="24d80-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="24d80-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="24d80-124">-StorageAccount</span></span>
<span data-ttu-id="24d80-125">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="24d80-125">Storage account object</span></span>

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

### <span data-ttu-id="24d80-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="24d80-126">-StorageAccountName</span></span>
<span data-ttu-id="24d80-127">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="24d80-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="24d80-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24d80-128">-Confirm</span></span>
<span data-ttu-id="24d80-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24d80-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d80-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d80-130">-WhatIf</span></span>
<span data-ttu-id="24d80-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24d80-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d80-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24d80-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d80-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d80-133">CommonParameters</span></span>
<span data-ttu-id="24d80-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d80-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d80-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d80-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d80-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24d80-136">INPUTS</span></span>

### <span data-ttu-id="24d80-137">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24d80-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="24d80-138">Microsoft. Azure. Commands. Management. storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="24d80-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="24d80-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24d80-139">OUTPUTS</span></span>

### <span data-ttu-id="24d80-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24d80-140">System.Boolean</span></span>

## <span data-ttu-id="24d80-141">Note</span><span class="sxs-lookup"><span data-stu-id="24d80-141">NOTES</span></span>

## <span data-ttu-id="24d80-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24d80-142">RELATED LINKS</span></span>
