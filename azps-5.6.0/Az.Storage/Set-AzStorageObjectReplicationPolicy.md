---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: e5d141672fe2f620fc86306b79069d309235393f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974157"
---
# <span data-ttu-id="5fb31-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="5fb31-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="5fb31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fb31-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb31-103">Crea o aggiorna i criteri di replica degli oggetti specificati in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5fb31-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="5fb31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fb31-104">SYNTAX</span></span>

### <span data-ttu-id="5fb31-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5fb31-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fb31-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="5fb31-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fb31-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5fb31-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fb31-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5fb31-108">DESCRIPTION</span></span>
<span data-ttu-id="5fb31-109">Il cmdlet **Set-AzStorageObjectReplicationPolicy** crea o aggiorna i criteri di replica degli oggetti specificati in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5fb31-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="5fb31-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fb31-110">EXAMPLES</span></span>

### <span data-ttu-id="5fb31-111">Esempio 1: Impostare i criteri di replica degli oggetti sia sull'account di destinazione che su quello di origine.</span><span class="sxs-lookup"><span data-stu-id="5fb31-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="5fb31-112">Questo comando imposta i criteri di replica degli oggetti sia sull'account di destinazione che su quello di origine.</span><span class="sxs-lookup"><span data-stu-id="5fb31-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="5fb31-113">Creare prima di tutto 2 regole dei criteri di replica degli oggetti e impostare il criterio con 2 regole per l'account di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5fb31-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="5fb31-114">Impostare quindi i criteri di replica degli oggetti dall'account di destinazione all'account di origine.</span><span class="sxs-lookup"><span data-stu-id="5fb31-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="5fb31-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fb31-115">PARAMETERS</span></span>

### <span data-ttu-id="5fb31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb31-116">-DefaultProfile</span></span>
<span data-ttu-id="5fb31-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fb31-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fb31-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="5fb31-118">-DestinationAccount</span></span>
<span data-ttu-id="5fb31-119">DestinationAccount dei criteri di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="5fb31-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb31-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fb31-120">-InputObject</span></span>
<span data-ttu-id="5fb31-121">Oggetto Criteri di replica degli oggetti da impostare sull'account specificato.</span><span class="sxs-lookup"><span data-stu-id="5fb31-121">Object Replication Policy Object to Set to the specified Account.</span></span>

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

### <span data-ttu-id="5fb31-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="5fb31-122">-PolicyId</span></span>
<span data-ttu-id="5fb31-123">ID dei criteri di replica degli oggetti. Deve essere un GUID o un valore "predefinito".</span><span class="sxs-lookup"><span data-stu-id="5fb31-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="5fb31-124">Se non input policyId, userà "predefinito", il che significa che per creare un nuovo criterio e l'ID del nuovo criterio verrà restituito nei criteri creati.</span><span class="sxs-lookup"><span data-stu-id="5fb31-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb31-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb31-125">-ResourceGroupName</span></span>
<span data-ttu-id="5fb31-126">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5fb31-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb31-127">-Rule</span><span class="sxs-lookup"><span data-stu-id="5fb31-127">-Rule</span></span>
<span data-ttu-id="5fb31-128">Regole dei criteri di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="5fb31-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb31-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="5fb31-129">-SourceAccount</span></span>
<span data-ttu-id="5fb31-130">SourceAccount dei criteri di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="5fb31-130">Object Replication Policy SourceAccount.</span></span>

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

### <span data-ttu-id="5fb31-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fb31-131">-StorageAccount</span></span>
<span data-ttu-id="5fb31-132">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5fb31-132">Storage account object</span></span>

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

### <span data-ttu-id="5fb31-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5fb31-133">-StorageAccountName</span></span>
<span data-ttu-id="5fb31-134">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5fb31-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb31-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fb31-135">-Confirm</span></span>
<span data-ttu-id="5fb31-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fb31-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb31-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb31-137">-WhatIf</span></span>
<span data-ttu-id="5fb31-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fb31-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fb31-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fb31-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb31-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb31-140">CommonParameters</span></span>
<span data-ttu-id="5fb31-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb31-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb31-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb31-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb31-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="5fb31-143">INPUTS</span></span>

### <span data-ttu-id="5fb31-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fb31-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5fb31-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="5fb31-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="5fb31-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fb31-146">OUTPUTS</span></span>

### <span data-ttu-id="5fb31-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="5fb31-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="5fb31-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="5fb31-148">NOTES</span></span>

## <span data-ttu-id="5fb31-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fb31-149">RELATED LINKS</span></span>
