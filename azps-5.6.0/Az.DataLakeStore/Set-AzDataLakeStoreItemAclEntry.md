---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2577f61476fd5026d75b677e35b994d64f4954e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956174"
---
# <span data-ttu-id="a0d27-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0d27-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="a0d27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0d27-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d27-103">Modifica una voce nell'elenco di controllo di accesso di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a0d27-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a0d27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0d27-104">SYNTAX</span></span>

### <span data-ttu-id="a0d27-105">SetByACLObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0d27-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d27-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="a0d27-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d27-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a0d27-107">DESCRIPTION</span></span>
<span data-ttu-id="a0d27-108">Il cmdlet **Set-AzDataLakeStoreItemAclEntry** modifica una voce (ACE) nell'elenco di controllo di accesso (ACL) di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a0d27-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a0d27-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0d27-109">EXAMPLES</span></span>

### <span data-ttu-id="a0d27-110">Esempio 1: Modificare le autorizzazioni per una ACE</span><span class="sxs-lookup"><span data-stu-id="a0d27-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="a0d27-111">Questo comando modifica l'elenco ACE per fare in modo che Patti Fuller abbia tutte le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="a0d27-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="a0d27-112">Esempio 2: Modificare le autorizzazioni per una ACE in modo ricorsivo</span><span class="sxs-lookup"><span data-stu-id="a0d27-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="a0d27-113">Esempio 3: Modificare le autorizzazioni per una ACE in modo ricorsivo usando un oggetto Acl</span><span class="sxs-lookup"><span data-stu-id="a0d27-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="a0d27-114">Questo comando modifica in modo ricorsivo l'elenco ACE per fare in modo che Patti Fuller abbia tutte le autorizzazioni per la radice e tutte le relative sottodirectory e file.</span><span class="sxs-lookup"><span data-stu-id="a0d27-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="a0d27-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0d27-115">PARAMETERS</span></span>

### <span data-ttu-id="a0d27-116">-Account</span><span class="sxs-lookup"><span data-stu-id="a0d27-116">-Account</span></span>
<span data-ttu-id="a0d27-117">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a0d27-117">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="a0d27-118">-AceType</span></span>
<span data-ttu-id="a0d27-119">Specifica il tipo di controllo di accesso da modificare.</span><span class="sxs-lookup"><span data-stu-id="a0d27-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="a0d27-120">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="a0d27-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0d27-121">Utente</span><span class="sxs-lookup"><span data-stu-id="a0d27-121">User</span></span> 
- <span data-ttu-id="a0d27-122">Raggruppa</span><span class="sxs-lookup"><span data-stu-id="a0d27-122">Group</span></span> 
- <span data-ttu-id="a0d27-123">Maschera</span><span class="sxs-lookup"><span data-stu-id="a0d27-123">Mask</span></span> 
- <span data-ttu-id="a0d27-124">Altro</span><span class="sxs-lookup"><span data-stu-id="a0d27-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="a0d27-125">-Acl</span></span>
<span data-ttu-id="a0d27-126">Specifica l'oggetto ACL che contiene le voci da modificare.</span><span class="sxs-lookup"><span data-stu-id="a0d27-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-127">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="a0d27-127">-Concurrency</span></span>
<span data-ttu-id="a0d27-128">Numero di file/directory elaborate in parallelo.</span><span class="sxs-lookup"><span data-stu-id="a0d27-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="a0d27-129">Facoltativo: verrà selezionata un'impostazione predefinita ragionevole</span><span class="sxs-lookup"><span data-stu-id="a0d27-129">Optional: a reasonable default will be selected</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-130">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="a0d27-130">-Default</span></span>
<span data-ttu-id="a0d27-131">Indica che questa operazione modifica l'elenco di controllo di accesso predefinito dall'ACL specificato.</span><span class="sxs-lookup"><span data-stu-id="a0d27-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d27-132">-DefaultProfile</span></span>
<span data-ttu-id="a0d27-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d27-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0d27-134">-Id</span><span class="sxs-lookup"><span data-stu-id="a0d27-134">-Id</span></span>
<span data-ttu-id="a0d27-135">Specifica l'ID oggetto dell'utente, gruppo o entità servizio di AzureActive Directory per cui modificare una ACE.</span><span class="sxs-lookup"><span data-stu-id="a0d27-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0d27-136">-PassThru</span></span>
<span data-ttu-id="a0d27-137">Indica che deve essere restituito l'ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="a0d27-137">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-138">-Path</span><span class="sxs-lookup"><span data-stu-id="a0d27-138">-Path</span></span>
<span data-ttu-id="a0d27-139">Specifica il percorso Data Lake Store dell'elemento per cui modificare una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="a0d27-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-140">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="a0d27-140">-Permissions</span></span>
<span data-ttu-id="a0d27-141">Specifica le autorizzazioni per l'elenco di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="a0d27-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="a0d27-142">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="a0d27-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0d27-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a0d27-143">None</span></span>
- <span data-ttu-id="a0d27-144">Esegui</span><span class="sxs-lookup"><span data-stu-id="a0d27-144">Execute</span></span>
- <span data-ttu-id="a0d27-145">Scrivere</span><span class="sxs-lookup"><span data-stu-id="a0d27-145">Write</span></span>
- <span data-ttu-id="a0d27-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="a0d27-146">WriteExecute</span></span>
- <span data-ttu-id="a0d27-147">Lettura</span><span class="sxs-lookup"><span data-stu-id="a0d27-147">Read</span></span>
- <span data-ttu-id="a0d27-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="a0d27-148">ReadExecute</span></span>
- <span data-ttu-id="a0d27-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a0d27-149">ReadWrite</span></span>
- <span data-ttu-id="a0d27-150">Tutti</span><span class="sxs-lookup"><span data-stu-id="a0d27-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-151">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="a0d27-151">-Recurse</span></span>
<span data-ttu-id="a0d27-152">Indica l'ACL da modificare in modo ricorsivo per i file e le sottodirectory figlio</span><span class="sxs-lookup"><span data-stu-id="a0d27-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d27-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="a0d27-153">-ShowProgress</span></span>
<span data-ttu-id="a0d27-154">Se viene superato, viene visualizzato lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="a0d27-154">If passed then progress status is showed.</span></span> <span data-ttu-id="a0d27-155">Applicabile solo quando viene eseguita la modifica ricorsiva dell'Acl.</span><span class="sxs-lookup"><span data-stu-id="a0d27-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="a0d27-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0d27-156">-Confirm</span></span>
<span data-ttu-id="a0d27-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d27-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d27-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d27-158">-WhatIf</span></span>
<span data-ttu-id="a0d27-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d27-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d27-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d27-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d27-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d27-161">CommonParameters</span></span>
<span data-ttu-id="a0d27-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d27-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d27-163">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d27-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d27-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="a0d27-164">INPUTS</span></span>

### <span data-ttu-id="a0d27-165">System.String</span><span class="sxs-lookup"><span data-stu-id="a0d27-165">System.String</span></span>

### <span data-ttu-id="a0d27-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a0d27-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a0d27-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="a0d27-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="a0d27-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="a0d27-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="a0d27-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a0d27-169">System.Guid</span></span>

### <span data-ttu-id="a0d27-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span><span class="sxs-lookup"><span data-stu-id="a0d27-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="a0d27-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0d27-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a0d27-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a0d27-172">System.Int32</span></span>

## <span data-ttu-id="a0d27-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0d27-173">OUTPUTS</span></span>

### <span data-ttu-id="a0d27-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="a0d27-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="a0d27-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="a0d27-175">NOTES</span></span>

## <span data-ttu-id="a0d27-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0d27-176">RELATED LINKS</span></span>

[<span data-ttu-id="a0d27-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0d27-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


