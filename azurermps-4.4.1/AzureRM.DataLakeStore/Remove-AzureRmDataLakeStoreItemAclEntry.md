---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 14e1dd0b897ce5f5c9557ed5aa72c3f63a6514f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687205"
---
# <span data-ttu-id="8fa82-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8fa82-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="8fa82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fa82-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa82-103">Consente di rimuovere una voce dall'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa82-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fa82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fa82-104">SYNTAX</span></span>

### <span data-ttu-id="8fa82-105">Rimuovere le voci ACL usando l'oggetto ACL (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8fa82-105">Remove ACL Entries using ACL object (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8fa82-106">Rimuovi ACE specifica</span><span class="sxs-lookup"><span data-stu-id="8fa82-106">Remove specific ACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fa82-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fa82-107">DESCRIPTION</span></span>
<span data-ttu-id="8fa82-108">Il cmdlet **Remove-AzureRmDataLakeStoreItemAclEntry** consente di rimuovere una voce (ACE) dall'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa82-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8fa82-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fa82-109">EXAMPLES</span></span>

### <span data-ttu-id="8fa82-110">Esempio 1: rimuovere una voce utente</span><span class="sxs-lookup"><span data-stu-id="8fa82-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="8fa82-111">Questo comando rimuove l'ACE utente per Patti Fuller dall'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="8fa82-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="8fa82-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fa82-112">PARAMETERS</span></span>

### <span data-ttu-id="8fa82-113">-Account</span><span class="sxs-lookup"><span data-stu-id="8fa82-113">-Account</span></span>
<span data-ttu-id="8fa82-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa82-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8fa82-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="8fa82-115">-AceType</span></span>
<span data-ttu-id="8fa82-116">Specifica il tipo di ACE da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8fa82-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="8fa82-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8fa82-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8fa82-118">Utente</span><span class="sxs-lookup"><span data-stu-id="8fa82-118">User</span></span>
- <span data-ttu-id="8fa82-119">Gruppo</span><span class="sxs-lookup"><span data-stu-id="8fa82-119">Group</span></span>
- <span data-ttu-id="8fa82-120">Maschera</span><span class="sxs-lookup"><span data-stu-id="8fa82-120">Mask</span></span>
- <span data-ttu-id="8fa82-121">Altri</span><span class="sxs-lookup"><span data-stu-id="8fa82-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Remove specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa82-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="8fa82-122">-Acl</span></span>
<span data-ttu-id="8fa82-123">Specifica l'oggetto ACL che contiene le voci da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8fa82-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Remove ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa82-124">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="8fa82-124">-Default</span></span>
<span data-ttu-id="8fa82-125">Indica che questa operazione rimuove l'ACE predefinita dall'ACL specificato.</span><span class="sxs-lookup"><span data-stu-id="8fa82-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa82-126">-ID</span><span class="sxs-lookup"><span data-stu-id="8fa82-126">-Id</span></span>
<span data-ttu-id="8fa82-127">Specifica l'ID oggetto dell'utente della directory AzureActive, del gruppo o dell'entità di servizio per cui rimuovere una voce ACE.</span><span class="sxs-lookup"><span data-stu-id="8fa82-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa82-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fa82-128">-PassThru</span></span>
<span data-ttu-id="8fa82-129">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="8fa82-129">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="8fa82-130">-Path</span><span class="sxs-lookup"><span data-stu-id="8fa82-130">-Path</span></span>
<span data-ttu-id="8fa82-131">Specifica il percorso dello Store Data Lake dell'elemento da cui rimuovere una voce ACE, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="8fa82-131">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8fa82-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8fa82-132">-Confirm</span></span>
<span data-ttu-id="8fa82-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fa82-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fa82-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fa82-134">-WhatIf</span></span>
<span data-ttu-id="8fa82-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fa82-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fa82-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fa82-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fa82-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa82-137">-DefaultProfile</span></span>
<span data-ttu-id="8fa82-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fa82-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fa82-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa82-139">CommonParameters</span></span>
<span data-ttu-id="8fa82-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa82-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa82-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa82-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa82-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fa82-142">INPUTS</span></span>

### <span data-ttu-id="8fa82-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="8fa82-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="8fa82-144">Il parametro "ACL" accetta il valore di tipo "DataLakeStoreItemAce []" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8fa82-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="8fa82-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fa82-145">OUTPUTS</span></span>

### <span data-ttu-id="8fa82-146">bool</span><span class="sxs-lookup"><span data-stu-id="8fa82-146">bool</span></span>
<span data-ttu-id="8fa82-147">Se PassThru è specificato, restituisce vero al completamento corretto.</span><span class="sxs-lookup"><span data-stu-id="8fa82-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="8fa82-148">Note</span><span class="sxs-lookup"><span data-stu-id="8fa82-148">NOTES</span></span>

## <span data-ttu-id="8fa82-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fa82-149">RELATED LINKS</span></span>

[<span data-ttu-id="8fa82-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8fa82-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


