---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: b6d07dbf390a0835bd28a045e4eea8bcf29e15f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209811"
---
# <span data-ttu-id="83d55-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="83d55-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="83d55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d55-102">SYNOPSIS</span></span>
<span data-ttu-id="83d55-103">Rimuove una voce dall'elenco di controllo di accesso di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="83d55-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="83d55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83d55-104">SYNTAX</span></span>

### <span data-ttu-id="83d55-105">RemoveByACLObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83d55-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83d55-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="83d55-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d55-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="83d55-107">DESCRIPTION</span></span>
<span data-ttu-id="83d55-108">Il cmdlet **Remove-AzDataLakeStoreItemAclEntry** rimuove una voce (ACE) dall'elenco di controllo di accesso (ACL) di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="83d55-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="83d55-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83d55-109">EXAMPLES</span></span>

### <span data-ttu-id="83d55-110">Esempio 1: Rimuovere una voce utente</span><span class="sxs-lookup"><span data-stu-id="83d55-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="83d55-111">Questo comando rimuove l'utente ACE per Patti Fuller dall'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="83d55-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="83d55-112">Esempio 2: Rimuovere una voce utente in modo ricorsivo</span><span class="sxs-lookup"><span data-stu-id="83d55-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="83d55-113">Esempio 3: Rimuovere le autorizzazioni per una ACE in modo ricorsivo usando l'oggetto Acl</span><span class="sxs-lookup"><span data-stu-id="83d55-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="83d55-114">Questo comando rimuove l'interfaccia di accesso utente per Patti Fuller dalla radice e in modo ricorsivo da tutte le sottodirectory e i file dell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="83d55-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="83d55-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83d55-115">PARAMETERS</span></span>

### <span data-ttu-id="83d55-116">-Account</span><span class="sxs-lookup"><span data-stu-id="83d55-116">-Account</span></span>
<span data-ttu-id="83d55-117">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="83d55-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="83d55-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="83d55-118">-AceType</span></span>
<span data-ttu-id="83d55-119">Specifica il tipo di controllo di accesso da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="83d55-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="83d55-120">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="83d55-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="83d55-121">Utente</span><span class="sxs-lookup"><span data-stu-id="83d55-121">User</span></span>
- <span data-ttu-id="83d55-122">Raggruppa</span><span class="sxs-lookup"><span data-stu-id="83d55-122">Group</span></span>
- <span data-ttu-id="83d55-123">Maschera</span><span class="sxs-lookup"><span data-stu-id="83d55-123">Mask</span></span>
- <span data-ttu-id="83d55-124">Altro</span><span class="sxs-lookup"><span data-stu-id="83d55-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d55-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="83d55-125">-Acl</span></span>
<span data-ttu-id="83d55-126">Specifica l'oggetto ACL che contiene le voci da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="83d55-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d55-127">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="83d55-127">-Concurrency</span></span>
<span data-ttu-id="83d55-128">Numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="83d55-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="83d55-129">Facoltativo: verrà selezionata un'impostazione predefinita ragionevole</span><span class="sxs-lookup"><span data-stu-id="83d55-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="83d55-130">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="83d55-130">-Default</span></span>
<span data-ttu-id="83d55-131">Indica che questa operazione rimuove l'elenco di controllo di accesso predefinito dall'elenco di controllo di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="83d55-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d55-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d55-132">-DefaultProfile</span></span>
<span data-ttu-id="83d55-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83d55-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83d55-134">-Id</span><span class="sxs-lookup"><span data-stu-id="83d55-134">-Id</span></span>
<span data-ttu-id="83d55-135">Specifica l'ID oggetto dell'utente, gruppo o entità servizio di AzureActive Directory per cui rimuovere una ACE.</span><span class="sxs-lookup"><span data-stu-id="83d55-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d55-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83d55-136">-PassThru</span></span>
<span data-ttu-id="83d55-137">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="83d55-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="83d55-138">-Path</span><span class="sxs-lookup"><span data-stu-id="83d55-138">-Path</span></span>
<span data-ttu-id="83d55-139">Specifica il percorso Data Lake Store dell'elemento da cui rimuovere una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="83d55-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="83d55-140">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="83d55-140">-Recurse</span></span>
<span data-ttu-id="83d55-141">Indica l'ACL da rimuovere in modo ricorsivo per i file e le sottodirectory figlio</span><span class="sxs-lookup"><span data-stu-id="83d55-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="83d55-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="83d55-142">-ShowProgress</span></span>
<span data-ttu-id="83d55-143">Se viene superato, viene visualizzato lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="83d55-143">If passed then progress status is showed.</span></span> <span data-ttu-id="83d55-144">Applicabile solo quando la rimozione ricorsiva dell'Acl viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="83d55-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="83d55-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83d55-145">-Confirm</span></span>
<span data-ttu-id="83d55-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83d55-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d55-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d55-147">-WhatIf</span></span>
<span data-ttu-id="83d55-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83d55-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d55-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83d55-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d55-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d55-150">CommonParameters</span></span>
<span data-ttu-id="83d55-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d55-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d55-152">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d55-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d55-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="83d55-153">INPUTS</span></span>

### <span data-ttu-id="83d55-154">System.String</span><span class="sxs-lookup"><span data-stu-id="83d55-154">System.String</span></span>

### <span data-ttu-id="83d55-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="83d55-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="83d55-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="83d55-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="83d55-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="83d55-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="83d55-158">System.Guid</span><span class="sxs-lookup"><span data-stu-id="83d55-158">System.Guid</span></span>

### <span data-ttu-id="83d55-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="83d55-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="83d55-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="83d55-160">System.Int32</span></span>

## <span data-ttu-id="83d55-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83d55-161">OUTPUTS</span></span>

### <span data-ttu-id="83d55-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="83d55-162">System.Boolean</span></span>

## <span data-ttu-id="83d55-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="83d55-163">NOTES</span></span>

## <span data-ttu-id="83d55-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83d55-164">RELATED LINKS</span></span>

[<span data-ttu-id="83d55-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="83d55-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


