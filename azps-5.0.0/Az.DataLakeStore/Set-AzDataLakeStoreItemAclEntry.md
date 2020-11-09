---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297750"
---
# <span data-ttu-id="37f27-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="37f27-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="37f27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37f27-102">SYNOPSIS</span></span>
<span data-ttu-id="37f27-103">Modifica una voce nell'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="37f27-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="37f27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37f27-104">SYNTAX</span></span>

### <span data-ttu-id="37f27-105">SetByACLObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="37f27-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37f27-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="37f27-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37f27-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37f27-107">DESCRIPTION</span></span>
<span data-ttu-id="37f27-108">Il cmdlet **set-AzDataLakeStoreItemAclEntry** modifica una voce (ACE) nell'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="37f27-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="37f27-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37f27-109">EXAMPLES</span></span>

### <span data-ttu-id="37f27-110">Esempio 1: modificare le autorizzazioni per una voce ACE</span><span class="sxs-lookup"><span data-stu-id="37f27-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="37f27-111">Questo comando modifica la voce ACE per Patti Fuller per avere tutte le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="37f27-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="37f27-112">Esempio 2: modificare le autorizzazioni per un'ACE in modo ricorsivo</span><span class="sxs-lookup"><span data-stu-id="37f27-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="37f27-113">Esempio 3: modificare le autorizzazioni per un ACE ricorsivamente usando l'oggetto ACL</span><span class="sxs-lookup"><span data-stu-id="37f27-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="37f27-114">Questo comando modifica ricorsivamente la voce ACE per Patti Fuller per avere tutte le autorizzazioni per radice e tutte le relative sottodirectory e file.</span><span class="sxs-lookup"><span data-stu-id="37f27-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="37f27-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37f27-115">PARAMETERS</span></span>

### <span data-ttu-id="37f27-116">-Account</span><span class="sxs-lookup"><span data-stu-id="37f27-116">-Account</span></span>
<span data-ttu-id="37f27-117">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="37f27-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="37f27-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="37f27-118">-AceType</span></span>
<span data-ttu-id="37f27-119">Specifica il tipo di ACE da modificare.</span><span class="sxs-lookup"><span data-stu-id="37f27-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="37f27-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="37f27-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37f27-121">Utente</span><span class="sxs-lookup"><span data-stu-id="37f27-121">User</span></span> 
- <span data-ttu-id="37f27-122">Gruppo</span><span class="sxs-lookup"><span data-stu-id="37f27-122">Group</span></span> 
- <span data-ttu-id="37f27-123">Maschera</span><span class="sxs-lookup"><span data-stu-id="37f27-123">Mask</span></span> 
- <span data-ttu-id="37f27-124">Altri</span><span class="sxs-lookup"><span data-stu-id="37f27-124">Other</span></span>

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

### <span data-ttu-id="37f27-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="37f27-125">-Acl</span></span>
<span data-ttu-id="37f27-126">Specifica l'oggetto ACL che contiene le voci da modificare.</span><span class="sxs-lookup"><span data-stu-id="37f27-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="37f27-127">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="37f27-127">-Concurrency</span></span>
<span data-ttu-id="37f27-128">Numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="37f27-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="37f27-129">Facoltativo: verrà selezionato un valore predefinito ragionevole</span><span class="sxs-lookup"><span data-stu-id="37f27-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="37f27-130">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="37f27-130">-Default</span></span>
<span data-ttu-id="37f27-131">Indica che questa operazione modifica la voce ACE predefinita dall'ACL specificato.</span><span class="sxs-lookup"><span data-stu-id="37f27-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="37f27-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f27-132">-DefaultProfile</span></span>
<span data-ttu-id="37f27-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37f27-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f27-134">-ID</span><span class="sxs-lookup"><span data-stu-id="37f27-134">-Id</span></span>
<span data-ttu-id="37f27-135">Specifica l'ID oggetto dell'utente della directory AzureActive, del gruppo o dell'entità di servizio per cui modificare una voce ACE.</span><span class="sxs-lookup"><span data-stu-id="37f27-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="37f27-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37f27-136">-PassThru</span></span>
<span data-ttu-id="37f27-137">Indica che deve essere restituito l'ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="37f27-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="37f27-138">-Path</span><span class="sxs-lookup"><span data-stu-id="37f27-138">-Path</span></span>
<span data-ttu-id="37f27-139">Specifica il percorso dello Store Data Lake dell'elemento per cui modificare una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="37f27-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="37f27-140">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="37f27-140">-Permissions</span></span>
<span data-ttu-id="37f27-141">Specifica le autorizzazioni per l'ACE.</span><span class="sxs-lookup"><span data-stu-id="37f27-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="37f27-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="37f27-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37f27-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="37f27-143">None</span></span>
- <span data-ttu-id="37f27-144">Eseguire</span><span class="sxs-lookup"><span data-stu-id="37f27-144">Execute</span></span>
- <span data-ttu-id="37f27-145">Scrivere</span><span class="sxs-lookup"><span data-stu-id="37f27-145">Write</span></span>
- <span data-ttu-id="37f27-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="37f27-146">WriteExecute</span></span>
- <span data-ttu-id="37f27-147">Leggere</span><span class="sxs-lookup"><span data-stu-id="37f27-147">Read</span></span>
- <span data-ttu-id="37f27-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="37f27-148">ReadExecute</span></span>
- <span data-ttu-id="37f27-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="37f27-149">ReadWrite</span></span>
- <span data-ttu-id="37f27-150">Tutti</span><span class="sxs-lookup"><span data-stu-id="37f27-150">All</span></span>

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

### <span data-ttu-id="37f27-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="37f27-151">-Recurse</span></span>
<span data-ttu-id="37f27-152">Indica che l'ACL deve essere modificato ricorsivamente nelle sottodirectory e nei file secondari</span><span class="sxs-lookup"><span data-stu-id="37f27-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="37f27-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="37f27-153">-ShowProgress</span></span>
<span data-ttu-id="37f27-154">Se viene passato lo stato di avanzamento viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="37f27-154">If passed then progress status is showed.</span></span> <span data-ttu-id="37f27-155">Applicabile solo quando viene eseguita la modifica ricorsiva ACL.</span><span class="sxs-lookup"><span data-stu-id="37f27-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="37f27-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37f27-156">-Confirm</span></span>
<span data-ttu-id="37f27-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37f27-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37f27-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37f27-158">-WhatIf</span></span>
<span data-ttu-id="37f27-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37f27-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37f27-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37f27-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37f27-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f27-161">CommonParameters</span></span>
<span data-ttu-id="37f27-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37f27-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f27-163">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37f27-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f27-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37f27-164">INPUTS</span></span>

### <span data-ttu-id="37f27-165">System. String</span><span class="sxs-lookup"><span data-stu-id="37f27-165">System.String</span></span>

### <span data-ttu-id="37f27-166">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="37f27-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="37f27-167">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="37f27-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="37f27-168">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="37f27-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="37f27-169">System. Guid</span><span class="sxs-lookup"><span data-stu-id="37f27-169">System.Guid</span></span>

### <span data-ttu-id="37f27-170">Autorizzazione Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums +</span><span class="sxs-lookup"><span data-stu-id="37f27-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="37f27-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="37f27-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="37f27-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="37f27-172">System.Int32</span></span>

## <span data-ttu-id="37f27-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37f27-173">OUTPUTS</span></span>

### <span data-ttu-id="37f27-174">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="37f27-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="37f27-175">Note</span><span class="sxs-lookup"><span data-stu-id="37f27-175">NOTES</span></span>

## <span data-ttu-id="37f27-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37f27-176">RELATED LINKS</span></span>

[<span data-ttu-id="37f27-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="37f27-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


