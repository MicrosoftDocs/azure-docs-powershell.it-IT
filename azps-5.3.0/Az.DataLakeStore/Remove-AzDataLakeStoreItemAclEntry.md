---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: b6d07dbf390a0835bd28a045e4eea8bcf29e15f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473557"
---
# <span data-ttu-id="d52c2-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d52c2-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="d52c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d52c2-102">SYNOPSIS</span></span>
<span data-ttu-id="d52c2-103">Consente di rimuovere una voce dall'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d52c2-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d52c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d52c2-104">SYNTAX</span></span>

### <span data-ttu-id="d52c2-105">RemoveByACLObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d52c2-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d52c2-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="d52c2-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d52c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d52c2-107">DESCRIPTION</span></span>
<span data-ttu-id="d52c2-108">Il cmdlet **Remove-AzDataLakeStoreItemAclEntry** consente di rimuovere una voce (ACE) dall'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d52c2-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d52c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d52c2-109">EXAMPLES</span></span>

### <span data-ttu-id="d52c2-110">Esempio 1: rimuovere una voce utente</span><span class="sxs-lookup"><span data-stu-id="d52c2-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="d52c2-111">Questo comando rimuove l'ACE utente per Patti Fuller dall'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="d52c2-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="d52c2-112">Esempio 2: rimuovere una voce di utente in modo ricorsivo</span><span class="sxs-lookup"><span data-stu-id="d52c2-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="d52c2-113">Esempio 3: rimuovere le autorizzazioni per un'ACE in modo ricorsivo usando l'oggetto ACL</span><span class="sxs-lookup"><span data-stu-id="d52c2-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="d52c2-114">Questo comando rimuove l'ACE utente per Patti Fuller dalla radice e ricorsivamente da tutte le sue sottodirectory e file per l'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="d52c2-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="d52c2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d52c2-115">PARAMETERS</span></span>

### <span data-ttu-id="d52c2-116">-Account</span><span class="sxs-lookup"><span data-stu-id="d52c2-116">-Account</span></span>
<span data-ttu-id="d52c2-117">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d52c2-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d52c2-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="d52c2-118">-AceType</span></span>
<span data-ttu-id="d52c2-119">Specifica il tipo di ACE da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d52c2-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="d52c2-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d52c2-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d52c2-121">Utente</span><span class="sxs-lookup"><span data-stu-id="d52c2-121">User</span></span>
- <span data-ttu-id="d52c2-122">Gruppo</span><span class="sxs-lookup"><span data-stu-id="d52c2-122">Group</span></span>
- <span data-ttu-id="d52c2-123">Maschera</span><span class="sxs-lookup"><span data-stu-id="d52c2-123">Mask</span></span>
- <span data-ttu-id="d52c2-124">Altri</span><span class="sxs-lookup"><span data-stu-id="d52c2-124">Other</span></span>

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

### <span data-ttu-id="d52c2-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="d52c2-125">-Acl</span></span>
<span data-ttu-id="d52c2-126">Specifica l'oggetto ACL che contiene le voci da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d52c2-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="d52c2-127">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="d52c2-127">-Concurrency</span></span>
<span data-ttu-id="d52c2-128">Numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="d52c2-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="d52c2-129">Facoltativo: verrà selezionato un valore predefinito ragionevole</span><span class="sxs-lookup"><span data-stu-id="d52c2-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="d52c2-130">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="d52c2-130">-Default</span></span>
<span data-ttu-id="d52c2-131">Indica che questa operazione rimuove l'ACE predefinita dall'ACL specificato.</span><span class="sxs-lookup"><span data-stu-id="d52c2-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="d52c2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d52c2-132">-DefaultProfile</span></span>
<span data-ttu-id="d52c2-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d52c2-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d52c2-134">-ID</span><span class="sxs-lookup"><span data-stu-id="d52c2-134">-Id</span></span>
<span data-ttu-id="d52c2-135">Specifica l'ID oggetto dell'utente della directory AzureActive, del gruppo o dell'entità di servizio per cui rimuovere una voce ACE.</span><span class="sxs-lookup"><span data-stu-id="d52c2-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="d52c2-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d52c2-136">-PassThru</span></span>
<span data-ttu-id="d52c2-137">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="d52c2-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d52c2-138">-Path</span><span class="sxs-lookup"><span data-stu-id="d52c2-138">-Path</span></span>
<span data-ttu-id="d52c2-139">Specifica il percorso dello Store Data Lake dell'elemento da cui rimuovere una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="d52c2-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d52c2-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="d52c2-140">-Recurse</span></span>
<span data-ttu-id="d52c2-141">Indica che l'ACL deve essere rimosso ricorsivamente nelle sottodirectory e nei file secondari</span><span class="sxs-lookup"><span data-stu-id="d52c2-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="d52c2-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="d52c2-142">-ShowProgress</span></span>
<span data-ttu-id="d52c2-143">Se viene passato lo stato di avanzamento viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="d52c2-143">If passed then progress status is showed.</span></span> <span data-ttu-id="d52c2-144">Applicabile solo quando è stata eseguita la rimozione ricorsiva ACL.</span><span class="sxs-lookup"><span data-stu-id="d52c2-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="d52c2-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d52c2-145">-Confirm</span></span>
<span data-ttu-id="d52c2-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d52c2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d52c2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d52c2-147">-WhatIf</span></span>
<span data-ttu-id="d52c2-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d52c2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d52c2-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d52c2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d52c2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d52c2-150">CommonParameters</span></span>
<span data-ttu-id="d52c2-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d52c2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d52c2-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d52c2-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d52c2-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d52c2-153">INPUTS</span></span>

### <span data-ttu-id="d52c2-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d52c2-154">System.String</span></span>

### <span data-ttu-id="d52c2-155">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d52c2-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d52c2-156">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="d52c2-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="d52c2-157">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="d52c2-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="d52c2-158">System. Guid</span><span class="sxs-lookup"><span data-stu-id="d52c2-158">System.Guid</span></span>

### <span data-ttu-id="d52c2-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d52c2-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d52c2-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d52c2-160">System.Int32</span></span>

## <span data-ttu-id="d52c2-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d52c2-161">OUTPUTS</span></span>

### <span data-ttu-id="d52c2-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d52c2-162">System.Boolean</span></span>

## <span data-ttu-id="d52c2-163">Note</span><span class="sxs-lookup"><span data-stu-id="d52c2-163">NOTES</span></span>

## <span data-ttu-id="d52c2-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d52c2-164">RELATED LINKS</span></span>

[<span data-ttu-id="d52c2-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d52c2-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


