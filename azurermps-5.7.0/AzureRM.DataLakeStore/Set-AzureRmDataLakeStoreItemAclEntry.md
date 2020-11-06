---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: cae7ac30d54be40be023025b9f45778d7c017583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509868"
---
# <span data-ttu-id="3edd5-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3edd5-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="3edd5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3edd5-102">SYNOPSIS</span></span>
<span data-ttu-id="3edd5-103">Modifica una voce nell'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3edd5-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3edd5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3edd5-104">SYNTAX</span></span>

### <span data-ttu-id="3edd5-105">SetByACLObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3edd5-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3edd5-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="3edd5-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3edd5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3edd5-107">DESCRIPTION</span></span>
<span data-ttu-id="3edd5-108">Il cmdlet **set-AzureRmDataLakeStoreItemAclEntry** modifica una voce (ACE) nell'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3edd5-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3edd5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3edd5-109">EXAMPLES</span></span>

### <span data-ttu-id="3edd5-110">Esempio 1: modificare le autorizzazioni per una voce ACE</span><span class="sxs-lookup"><span data-stu-id="3edd5-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="3edd5-111">Questo comando modifica la voce ACE per Patti Fuller per avere tutte le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="3edd5-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="3edd5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3edd5-112">PARAMETERS</span></span>

### <span data-ttu-id="3edd5-113">-Account</span><span class="sxs-lookup"><span data-stu-id="3edd5-113">-Account</span></span>
<span data-ttu-id="3edd5-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3edd5-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="3edd5-115">-AceType</span></span>
<span data-ttu-id="3edd5-116">Specifica il tipo di ACE da modificare.</span><span class="sxs-lookup"><span data-stu-id="3edd5-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="3edd5-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3edd5-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3edd5-118">Utente</span><span class="sxs-lookup"><span data-stu-id="3edd5-118">User</span></span> 
- <span data-ttu-id="3edd5-119">Gruppo</span><span class="sxs-lookup"><span data-stu-id="3edd5-119">Group</span></span> 
- <span data-ttu-id="3edd5-120">Maschera</span><span class="sxs-lookup"><span data-stu-id="3edd5-120">Mask</span></span> 
- <span data-ttu-id="3edd5-121">Altri</span><span class="sxs-lookup"><span data-stu-id="3edd5-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: SetSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="3edd5-122">-Acl</span></span>
<span data-ttu-id="3edd5-123">Specifica l'oggetto ACL che contiene le voci da modificare.</span><span class="sxs-lookup"><span data-stu-id="3edd5-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-124">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="3edd5-124">-Default</span></span>
<span data-ttu-id="3edd5-125">Indica che questa operazione modifica la voce ACE predefinita dall'ACL specificato.</span><span class="sxs-lookup"><span data-stu-id="3edd5-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edd5-126">-DefaultProfile</span></span>
<span data-ttu-id="3edd5-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3edd5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-128">-ID</span><span class="sxs-lookup"><span data-stu-id="3edd5-128">-Id</span></span>
<span data-ttu-id="3edd5-129">Specifica l'ID oggetto dell'utente della directory AzureActive, del gruppo o dell'entità di servizio per cui modificare una voce ACE.</span><span class="sxs-lookup"><span data-stu-id="3edd5-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3edd5-130">-PassThru</span></span>
<span data-ttu-id="3edd5-131">Indica che deve essere restituito l'ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="3edd5-131">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-132">-Path</span><span class="sxs-lookup"><span data-stu-id="3edd5-132">-Path</span></span>
<span data-ttu-id="3edd5-133">Specifica il percorso dello Store Data Lake dell'elemento per cui modificare una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="3edd5-133">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-134">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="3edd5-134">-Permissions</span></span>
<span data-ttu-id="3edd5-135">Specifica le autorizzazioni per l'ACE.</span><span class="sxs-lookup"><span data-stu-id="3edd5-135">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="3edd5-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3edd5-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3edd5-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3edd5-137">None</span></span>
- <span data-ttu-id="3edd5-138">Eseguire</span><span class="sxs-lookup"><span data-stu-id="3edd5-138">Execute</span></span>
- <span data-ttu-id="3edd5-139">Scrivere</span><span class="sxs-lookup"><span data-stu-id="3edd5-139">Write</span></span>
- <span data-ttu-id="3edd5-140">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="3edd5-140">WriteExecute</span></span>
- <span data-ttu-id="3edd5-141">Leggere</span><span class="sxs-lookup"><span data-stu-id="3edd5-141">Read</span></span>
- <span data-ttu-id="3edd5-142">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="3edd5-142">ReadExecute</span></span>
- <span data-ttu-id="3edd5-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3edd5-143">ReadWrite</span></span>
- <span data-ttu-id="3edd5-144">Tutti</span><span class="sxs-lookup"><span data-stu-id="3edd5-144">All</span></span>

```yaml
Type: Permission
Parameter Sets: SetSpecificACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3edd5-145">-Confirm</span></span>
<span data-ttu-id="3edd5-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3edd5-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3edd5-147">-WhatIf</span></span>
<span data-ttu-id="3edd5-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3edd5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3edd5-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3edd5-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edd5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edd5-150">CommonParameters</span></span>
<span data-ttu-id="3edd5-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3edd5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edd5-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3edd5-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edd5-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3edd5-153">INPUTS</span></span>

### <span data-ttu-id="3edd5-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="3edd5-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="3edd5-155">Il parametro "ACL" accetta il valore di tipo "DataLakeStoreItemAce []" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3edd5-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="3edd5-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3edd5-156">OUTPUTS</span></span>

### <span data-ttu-id="3edd5-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="3edd5-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="3edd5-158">Se si specifica PassThru, verrà restituito l'elenco di voci ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="3edd5-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="3edd5-159">Note</span><span class="sxs-lookup"><span data-stu-id="3edd5-159">NOTES</span></span>

## <span data-ttu-id="3edd5-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3edd5-160">RELATED LINKS</span></span>

[<span data-ttu-id="3edd5-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3edd5-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


