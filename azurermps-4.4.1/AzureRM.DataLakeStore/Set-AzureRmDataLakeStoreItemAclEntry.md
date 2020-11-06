---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 9646ef98499e56e24ce81c78f6b94dce75ff0078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521251"
---
# <span data-ttu-id="ae6a8-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ae6a8-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="ae6a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6a8-103">Modifica una voce nell'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae6a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae6a8-104">SYNTAX</span></span>

### <span data-ttu-id="ae6a8-105">Impostare le voci ACL tramite l'oggetto ACL (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae6a8-105">Set ACL Entries using ACL object (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae6a8-106">Impostare una specifica ACE</span><span class="sxs-lookup"><span data-stu-id="ae6a8-106">Set specific ACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae6a8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae6a8-107">DESCRIPTION</span></span>
<span data-ttu-id="ae6a8-108">Il cmdlet **set-AzureRmDataLakeStoreItemAclEntry** modifica una voce (ACE) nell'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ae6a8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae6a8-109">EXAMPLES</span></span>

### <span data-ttu-id="ae6a8-110">Esempio 1: modificare le autorizzazioni per una voce ACE</span><span class="sxs-lookup"><span data-stu-id="ae6a8-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="ae6a8-111">Questo comando modifica la voce ACE per Patti Fuller per avere tutte le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="ae6a8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae6a8-112">PARAMETERS</span></span>

### <span data-ttu-id="ae6a8-113">-Account</span><span class="sxs-lookup"><span data-stu-id="ae6a8-113">-Account</span></span>
<span data-ttu-id="ae6a8-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ae6a8-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="ae6a8-115">-AceType</span></span>
<span data-ttu-id="ae6a8-116">Specifica il tipo di ACE da modificare.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="ae6a8-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae6a8-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae6a8-118">Utente</span><span class="sxs-lookup"><span data-stu-id="ae6a8-118">User</span></span> 
- <span data-ttu-id="ae6a8-119">Gruppo</span><span class="sxs-lookup"><span data-stu-id="ae6a8-119">Group</span></span> 
- <span data-ttu-id="ae6a8-120">Maschera</span><span class="sxs-lookup"><span data-stu-id="ae6a8-120">Mask</span></span> 
- <span data-ttu-id="ae6a8-121">Altri</span><span class="sxs-lookup"><span data-stu-id="ae6a8-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Set specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6a8-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="ae6a8-122">-Acl</span></span>
<span data-ttu-id="ae6a8-123">Specifica l'oggetto ACL che contiene le voci da modificare.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Set ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6a8-124">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="ae6a8-124">-Default</span></span>
<span data-ttu-id="ae6a8-125">Indica che questa operazione modifica la voce ACE predefinita dall'ACL specificato.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6a8-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ae6a8-126">-Id</span></span>
<span data-ttu-id="ae6a8-127">Specifica l'ID oggetto dell'utente della directory AzureActive, del gruppo o dell'entità di servizio per cui modificare una voce ACE.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6a8-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae6a8-128">-PassThru</span></span>
<span data-ttu-id="ae6a8-129">Indica che deve essere restituito l'ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-129">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="ae6a8-130">-Path</span><span class="sxs-lookup"><span data-stu-id="ae6a8-130">-Path</span></span>
<span data-ttu-id="ae6a8-131">Specifica il percorso dello Store Data Lake dell'elemento per cui modificare una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="ae6a8-131">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ae6a8-132">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="ae6a8-132">-Permissions</span></span>
<span data-ttu-id="ae6a8-133">Specifica le autorizzazioni per l'ACE.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-133">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="ae6a8-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae6a8-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae6a8-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ae6a8-135">None</span></span>
- <span data-ttu-id="ae6a8-136">Eseguire</span><span class="sxs-lookup"><span data-stu-id="ae6a8-136">Execute</span></span>
- <span data-ttu-id="ae6a8-137">Scrivere</span><span class="sxs-lookup"><span data-stu-id="ae6a8-137">Write</span></span>
- <span data-ttu-id="ae6a8-138">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="ae6a8-138">WriteExecute</span></span>
- <span data-ttu-id="ae6a8-139">Leggere</span><span class="sxs-lookup"><span data-stu-id="ae6a8-139">Read</span></span>
- <span data-ttu-id="ae6a8-140">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="ae6a8-140">ReadExecute</span></span>
- <span data-ttu-id="ae6a8-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ae6a8-141">ReadWrite</span></span>
- <span data-ttu-id="ae6a8-142">Tutti</span><span class="sxs-lookup"><span data-stu-id="ae6a8-142">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: Set specific ACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6a8-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae6a8-143">-Confirm</span></span>
<span data-ttu-id="ae6a8-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae6a8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae6a8-145">-WhatIf</span></span>
<span data-ttu-id="ae6a8-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae6a8-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae6a8-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6a8-148">-DefaultProfile</span></span>
<span data-ttu-id="ae6a8-149">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae6a8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6a8-150">CommonParameters</span></span>
<span data-ttu-id="ae6a8-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6a8-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6a8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6a8-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae6a8-153">INPUTS</span></span>

### <span data-ttu-id="ae6a8-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="ae6a8-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="ae6a8-155">Il parametro "ACL" accetta il valore di tipo "DataLakeStoreItemAce []" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ae6a8-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="ae6a8-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae6a8-156">OUTPUTS</span></span>

### <span data-ttu-id="ae6a8-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="ae6a8-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="ae6a8-158">Se si specifica PassThru, verrà restituito l'elenco di voci ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="ae6a8-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="ae6a8-159">Note</span><span class="sxs-lookup"><span data-stu-id="ae6a8-159">NOTES</span></span>

## <span data-ttu-id="ae6a8-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae6a8-160">RELATED LINKS</span></span>

[<span data-ttu-id="ae6a8-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ae6a8-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


