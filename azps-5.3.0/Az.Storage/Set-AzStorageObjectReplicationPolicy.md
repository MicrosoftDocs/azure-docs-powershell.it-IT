---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376123"
---
# <span data-ttu-id="1f4f1-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="1f4f1-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="1f4f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f4f1-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4f1-103">Crea o aggiorna i criteri di replica degli oggetti specificati in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="1f4f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f4f1-104">SYNTAX</span></span>

### <span data-ttu-id="1f4f1-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f4f1-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f4f1-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="1f4f1-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f4f1-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1f4f1-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f4f1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f4f1-108">DESCRIPTION</span></span>
<span data-ttu-id="1f4f1-109">Il cmdlet **set-AzStorageObjectReplicationPolicy** crea o aggiorna i criteri di replica degli oggetti specificati in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="1f4f1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f4f1-110">EXAMPLES</span></span>

### <span data-ttu-id="1f4f1-111">Esempio 1: impostare i criteri di replica degli oggetti sia per l'account di destinazione che per quello di origine.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-111">Example 1: Set object replication policy to both destination and source account.</span></span>
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

<span data-ttu-id="1f4f1-112">Questo comando imposta i criteri di replica degli oggetti sia per l'account di destinazione che per quello di origine.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="1f4f1-113">Prima di tutto creare due regole dei criteri di replica degli oggetti e impostare i criteri con l'account di destinazione 2 regole.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="1f4f1-114">Imposta quindi il criterio di replica degli oggetti dall'account di destinazione all'account di origine.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="1f4f1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f4f1-115">PARAMETERS</span></span>

### <span data-ttu-id="1f4f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4f1-116">-DefaultProfile</span></span>
<span data-ttu-id="1f4f1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f4f1-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="1f4f1-118">-DestinationAccount</span></span>
<span data-ttu-id="1f4f1-119">Criteri di replica degli oggetti DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-119">Object Replication Policy DestinationAccount.</span></span>

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

### <span data-ttu-id="1f4f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f4f1-120">-InputObject</span></span>
<span data-ttu-id="1f4f1-121">Oggetto Criteri di replica degli oggetti da impostare sull'account specificato.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-121">Object Replication Policy Object to Set to the specified Account.</span></span>

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

### <span data-ttu-id="1f4f1-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="1f4f1-122">-PolicyId</span></span>
<span data-ttu-id="1f4f1-123">ID criterio di replica degli oggetti. Dovrebbe essere un GUID o "default".</span><span class="sxs-lookup"><span data-stu-id="1f4f1-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="1f4f1-124">Se non viene inserito il PolicyId, verrà usato "default", che significa creare un nuovo criterio e l'ID del nuovo criterio verrà restituito nel criterio creato.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

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

### <span data-ttu-id="1f4f1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4f1-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f4f1-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="1f4f1-127">-Regola</span><span class="sxs-lookup"><span data-stu-id="1f4f1-127">-Rule</span></span>
<span data-ttu-id="1f4f1-128">Regole dei criteri di replica degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-128">Object Replication Policy Rules.</span></span>

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

### <span data-ttu-id="1f4f1-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="1f4f1-129">-SourceAccount</span></span>
<span data-ttu-id="1f4f1-130">Criteri di replica degli oggetti SourceAccount.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-130">Object Replication Policy SourceAccount.</span></span>

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

### <span data-ttu-id="1f4f1-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1f4f1-131">-StorageAccount</span></span>
<span data-ttu-id="1f4f1-132">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1f4f1-132">Storage account object</span></span>

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

### <span data-ttu-id="1f4f1-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1f4f1-133">-StorageAccountName</span></span>
<span data-ttu-id="1f4f1-134">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="1f4f1-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f4f1-135">-Confirm</span></span>
<span data-ttu-id="1f4f1-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f4f1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f4f1-137">-WhatIf</span></span>
<span data-ttu-id="1f4f1-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f4f1-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f4f1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4f1-140">CommonParameters</span></span>
<span data-ttu-id="1f4f1-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f4f1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4f1-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f4f1-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4f1-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f4f1-143">INPUTS</span></span>

### <span data-ttu-id="1f4f1-144">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1f4f1-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1f4f1-145">Microsoft. Azure. Commands. Management. storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="1f4f1-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="1f4f1-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f4f1-146">OUTPUTS</span></span>

### <span data-ttu-id="1f4f1-147">Microsoft. Azure. Commands. Management. storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="1f4f1-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="1f4f1-148">Note</span><span class="sxs-lookup"><span data-stu-id="1f4f1-148">NOTES</span></span>

## <span data-ttu-id="1f4f1-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f4f1-149">RELATED LINKS</span></span>
