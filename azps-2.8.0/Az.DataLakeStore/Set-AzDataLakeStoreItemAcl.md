---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 53cf81c4996a9d77d1452ffd6d5f99c111aecbf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674763"
---
# <span data-ttu-id="0995a-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="0995a-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="0995a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0995a-102">SYNOPSIS</span></span>
<span data-ttu-id="0995a-103">Modifica l'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0995a-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0995a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0995a-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0995a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0995a-105">DESCRIPTION</span></span>
<span data-ttu-id="0995a-106">Il cmdlet **set-AzDataLakeStoreItemAcl** modifica l'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0995a-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0995a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0995a-107">EXAMPLES</span></span>

### <span data-ttu-id="0995a-108">Esempio 1: impostare l'ACL per un file e una cartella</span><span class="sxs-lookup"><span data-stu-id="0995a-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="0995a-109">Il primo comando ottiene l'ACL per la directory radice dell'account ContosoADL e lo archivia nella variabile $ACL.</span><span class="sxs-lookup"><span data-stu-id="0995a-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="0995a-110">Il secondo comando imposta l'ACL per il file Test.txt a quella in $ACL.</span><span class="sxs-lookup"><span data-stu-id="0995a-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="0995a-111">Esempio 2: impostare l'ACL per la cartella ricorsivamente</span><span class="sxs-lookup"><span data-stu-id="0995a-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="0995a-112">Il primo comando ottiene l'ACL per la directory Cartella1 dell'account ContosoADL e lo archivia nella variabile $ACL.</span><span class="sxs-lookup"><span data-stu-id="0995a-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="0995a-113">Il secondo comando imposta l'ACL in modo ricorsivo in Cartella2 e nelle relative directory secondarie e file a quello di $ACL.</span><span class="sxs-lookup"><span data-stu-id="0995a-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="0995a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0995a-114">PARAMETERS</span></span>

### <span data-ttu-id="0995a-115">-Account</span><span class="sxs-lookup"><span data-stu-id="0995a-115">-Account</span></span>
<span data-ttu-id="0995a-116">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0995a-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0995a-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="0995a-117">-Acl</span></span>
<span data-ttu-id="0995a-118">Specifica un ACL per un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="0995a-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0995a-119">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="0995a-119">-Concurrency</span></span>
<span data-ttu-id="0995a-120">Numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="0995a-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="0995a-121">Facoltativo: verrà selezionato un valore predefinito ragionevole.</span><span class="sxs-lookup"><span data-stu-id="0995a-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="0995a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0995a-122">-DefaultProfile</span></span>
<span data-ttu-id="0995a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0995a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0995a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0995a-124">-PassThru</span></span>
<span data-ttu-id="0995a-125">Indica che deve essere restituito l'ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="0995a-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="0995a-126">-Path</span><span class="sxs-lookup"><span data-stu-id="0995a-126">-Path</span></span>
<span data-ttu-id="0995a-127">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="0995a-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0995a-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="0995a-128">-Recurse</span></span>
<span data-ttu-id="0995a-129">Indica che l'ACL deve essere impostato ricorsivamente per le sottodirectory e i file secondari</span><span class="sxs-lookup"><span data-stu-id="0995a-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="0995a-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="0995a-130">-ShowProgress</span></span>
<span data-ttu-id="0995a-131">Se viene passato lo stato di avanzamento viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="0995a-131">If passed then progress status is showed.</span></span> <span data-ttu-id="0995a-132">Applicabile solo quando è stato eseguito un set di ACL ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="0995a-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="0995a-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0995a-133">-Confirm</span></span>
<span data-ttu-id="0995a-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0995a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0995a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0995a-135">-WhatIf</span></span>
<span data-ttu-id="0995a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0995a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0995a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0995a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0995a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0995a-138">CommonParameters</span></span>
<span data-ttu-id="0995a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0995a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0995a-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0995a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0995a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0995a-141">INPUTS</span></span>

### <span data-ttu-id="0995a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0995a-142">System.String</span></span>

### <span data-ttu-id="0995a-143">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0995a-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0995a-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="0995a-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="0995a-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0995a-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0995a-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0995a-146">System.Int32</span></span>

## <span data-ttu-id="0995a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0995a-147">OUTPUTS</span></span>

### <span data-ttu-id="0995a-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="0995a-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="0995a-149">Note</span><span class="sxs-lookup"><span data-stu-id="0995a-149">NOTES</span></span>

## <span data-ttu-id="0995a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0995a-150">RELATED LINKS</span></span>
