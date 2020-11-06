---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 154c57c6a403fce574a785aaf60d95a7936907b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507483"
---
# <span data-ttu-id="95fe3-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="95fe3-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="95fe3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="95fe3-103">Consente di rimuovere una voce dall'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95fe3-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95fe3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95fe3-104">SYNTAX</span></span>

### <span data-ttu-id="95fe3-105">RemoveByACLObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="95fe3-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95fe3-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="95fe3-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95fe3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95fe3-107">DESCRIPTION</span></span>
<span data-ttu-id="95fe3-108">Il cmdlet **Remove-AzureRmDataLakeStoreItemAclEntry** consente di rimuovere una voce (ACE) dall'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95fe3-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="95fe3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95fe3-109">EXAMPLES</span></span>

### <span data-ttu-id="95fe3-110">Esempio 1: rimuovere una voce utente</span><span class="sxs-lookup"><span data-stu-id="95fe3-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="95fe3-111">Questo comando rimuove l'ACE utente per Patti Fuller dall'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="95fe3-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="95fe3-112">Esempio 2: rimuovere una voce di utente in modo ricorsivo</span><span class="sxs-lookup"><span data-stu-id="95fe3-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="95fe3-113">Esempio 3: rimuovere le autorizzazioni per un'ACE in modo ricorsivo usando l'oggetto ACL</span><span class="sxs-lookup"><span data-stu-id="95fe3-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="95fe3-114">Questo comando rimuove l'ACE utente per Patti Fuller dalla radice e ricorsivamente da tutte le sue sottodirectory e file per l'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="95fe3-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="95fe3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95fe3-115">PARAMETERS</span></span>

### <span data-ttu-id="95fe3-116">-Account</span><span class="sxs-lookup"><span data-stu-id="95fe3-116">-Account</span></span>
<span data-ttu-id="95fe3-117">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95fe3-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="95fe3-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="95fe3-118">-AceType</span></span>
<span data-ttu-id="95fe3-119">Specifica il tipo di ACE da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="95fe3-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="95fe3-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="95fe3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95fe3-121">Utente</span><span class="sxs-lookup"><span data-stu-id="95fe3-121">User</span></span>
- <span data-ttu-id="95fe3-122">Gruppo</span><span class="sxs-lookup"><span data-stu-id="95fe3-122">Group</span></span>
- <span data-ttu-id="95fe3-123">Maschera</span><span class="sxs-lookup"><span data-stu-id="95fe3-123">Mask</span></span>
- <span data-ttu-id="95fe3-124">Altri</span><span class="sxs-lookup"><span data-stu-id="95fe3-124">Other</span></span>

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

### <span data-ttu-id="95fe3-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="95fe3-125">-Acl</span></span>
<span data-ttu-id="95fe3-126">Specifica l'oggetto ACL che contiene le voci da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="95fe3-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="95fe3-127">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="95fe3-127">-Concurrency</span></span>
<span data-ttu-id="95fe3-128">Numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="95fe3-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="95fe3-129">Facoltativo: verrà selezionato un valore predefinito ragionevole</span><span class="sxs-lookup"><span data-stu-id="95fe3-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="95fe3-130">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="95fe3-130">-Default</span></span>
<span data-ttu-id="95fe3-131">Indica che questa operazione rimuove l'ACE predefinita dall'ACL specificato.</span><span class="sxs-lookup"><span data-stu-id="95fe3-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="95fe3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fe3-132">-DefaultProfile</span></span>
<span data-ttu-id="95fe3-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95fe3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95fe3-134">-ID</span><span class="sxs-lookup"><span data-stu-id="95fe3-134">-Id</span></span>
<span data-ttu-id="95fe3-135">Specifica l'ID oggetto dell'utente della directory AzureActive, del gruppo o dell'entità di servizio per cui rimuovere una voce ACE.</span><span class="sxs-lookup"><span data-stu-id="95fe3-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="95fe3-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95fe3-136">-PassThru</span></span>
<span data-ttu-id="95fe3-137">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="95fe3-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="95fe3-138">-Path</span><span class="sxs-lookup"><span data-stu-id="95fe3-138">-Path</span></span>
<span data-ttu-id="95fe3-139">Specifica il percorso dello Store Data Lake dell'elemento da cui rimuovere una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="95fe3-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="95fe3-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="95fe3-140">-Recurse</span></span>
<span data-ttu-id="95fe3-141">Indica che l'ACL deve essere rimosso ricorsivamente nelle sottodirectory e nei file secondari</span><span class="sxs-lookup"><span data-stu-id="95fe3-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="95fe3-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="95fe3-142">-ShowProgress</span></span>
<span data-ttu-id="95fe3-143">Se viene passato lo stato di avanzamento viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="95fe3-143">If passed then progress status is showed.</span></span> <span data-ttu-id="95fe3-144">Applicabile solo quando è stata eseguita la rimozione ricorsiva ACL.</span><span class="sxs-lookup"><span data-stu-id="95fe3-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="95fe3-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="95fe3-145">-Confirm</span></span>
<span data-ttu-id="95fe3-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95fe3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95fe3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95fe3-147">-WhatIf</span></span>
<span data-ttu-id="95fe3-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95fe3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95fe3-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95fe3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95fe3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fe3-150">CommonParameters</span></span>
<span data-ttu-id="95fe3-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95fe3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fe3-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95fe3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fe3-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95fe3-153">INPUTS</span></span>

### <span data-ttu-id="95fe3-154">System. String</span><span class="sxs-lookup"><span data-stu-id="95fe3-154">System.String</span></span>

### <span data-ttu-id="95fe3-155">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="95fe3-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="95fe3-156">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="95fe3-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="95fe3-157">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="95fe3-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="95fe3-158">System. Guid</span><span class="sxs-lookup"><span data-stu-id="95fe3-158">System.Guid</span></span>

### <span data-ttu-id="95fe3-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="95fe3-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="95fe3-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="95fe3-160">System.Int32</span></span>

## <span data-ttu-id="95fe3-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95fe3-161">OUTPUTS</span></span>

### <span data-ttu-id="95fe3-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95fe3-162">System.Boolean</span></span>

## <span data-ttu-id="95fe3-163">Note</span><span class="sxs-lookup"><span data-stu-id="95fe3-163">NOTES</span></span>

## <span data-ttu-id="95fe3-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95fe3-164">RELATED LINKS</span></span>

[<span data-ttu-id="95fe3-165">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="95fe3-165">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


