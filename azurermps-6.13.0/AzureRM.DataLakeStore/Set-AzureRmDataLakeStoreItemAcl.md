---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 45bf9fe3fb57eb6e627f1b2c7bc3e9146ccfd444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515379"
---
# <span data-ttu-id="55cb4-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="55cb4-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="55cb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="55cb4-103">Modifica l'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55cb4-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55cb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55cb4-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55cb4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="55cb4-106">Il cmdlet **set-AzureRmDataLakeStoreItemAcl** modifica l'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55cb4-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="55cb4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55cb4-107">EXAMPLES</span></span>

### <span data-ttu-id="55cb4-108">Esempio 1: impostare l'ACL per un file e una cartella</span><span class="sxs-lookup"><span data-stu-id="55cb4-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="55cb4-109">Il primo comando ottiene l'ACL per la directory radice dell'account ContosoADL e lo archivia nella variabile $ACL.</span><span class="sxs-lookup"><span data-stu-id="55cb4-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="55cb4-110">Il secondo comando imposta l'ACL per il file Test.txt a quella in $ACL.</span><span class="sxs-lookup"><span data-stu-id="55cb4-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="55cb4-111">Esempio 2: impostare l'ACL per la cartella ricorsivamente</span><span class="sxs-lookup"><span data-stu-id="55cb4-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="55cb4-112">Il primo comando ottiene l'ACL per la directory Cartella1 dell'account ContosoADL e lo archivia nella variabile $ACL.</span><span class="sxs-lookup"><span data-stu-id="55cb4-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="55cb4-113">Il secondo comando imposta l'ACL in modo ricorsivo in Cartella2 e nelle relative directory secondarie e file a quello di $ACL.</span><span class="sxs-lookup"><span data-stu-id="55cb4-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="55cb4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55cb4-114">PARAMETERS</span></span>

### <span data-ttu-id="55cb4-115">-Account</span><span class="sxs-lookup"><span data-stu-id="55cb4-115">-Account</span></span>
<span data-ttu-id="55cb4-116">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55cb4-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="55cb4-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="55cb4-117">-Acl</span></span>
<span data-ttu-id="55cb4-118">Specifica un ACL per un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="55cb4-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="55cb4-119">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="55cb4-119">-Concurrency</span></span>
<span data-ttu-id="55cb4-120">Numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="55cb4-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="55cb4-121">Facoltativo: verrà selezionato un valore predefinito ragionevole.</span><span class="sxs-lookup"><span data-stu-id="55cb4-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="55cb4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55cb4-122">-DefaultProfile</span></span>
<span data-ttu-id="55cb4-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55cb4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55cb4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55cb4-124">-PassThru</span></span>
<span data-ttu-id="55cb4-125">Indica che deve essere restituito l'ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="55cb4-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="55cb4-126">-Path</span><span class="sxs-lookup"><span data-stu-id="55cb4-126">-Path</span></span>
<span data-ttu-id="55cb4-127">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="55cb4-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="55cb4-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="55cb4-128">-Recurse</span></span>
<span data-ttu-id="55cb4-129">Indica che l'ACL deve essere impostato ricorsivamente per le sottodirectory e i file secondari</span><span class="sxs-lookup"><span data-stu-id="55cb4-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="55cb4-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="55cb4-130">-ShowProgress</span></span>
<span data-ttu-id="55cb4-131">Se viene passato lo stato di avanzamento viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="55cb4-131">If passed then progress status is showed.</span></span> <span data-ttu-id="55cb4-132">Applicabile solo quando è stato eseguito un set di ACL ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="55cb4-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="55cb4-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="55cb4-133">-Confirm</span></span>
<span data-ttu-id="55cb4-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55cb4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55cb4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55cb4-135">-WhatIf</span></span>
<span data-ttu-id="55cb4-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55cb4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55cb4-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55cb4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55cb4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55cb4-138">CommonParameters</span></span>
<span data-ttu-id="55cb4-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55cb4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55cb4-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55cb4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55cb4-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55cb4-141">INPUTS</span></span>

### <span data-ttu-id="55cb4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="55cb4-142">System.String</span></span>

### <span data-ttu-id="55cb4-143">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="55cb4-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="55cb4-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="55cb4-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="55cb4-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55cb4-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="55cb4-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="55cb4-146">System.Int32</span></span>

## <span data-ttu-id="55cb4-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55cb4-147">OUTPUTS</span></span>

### <span data-ttu-id="55cb4-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="55cb4-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>
<span data-ttu-id="55cb4-149">Se si specifica PassThru, verrà restituito l'elenco di voci ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="55cb4-149">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="55cb4-150">Note</span><span class="sxs-lookup"><span data-stu-id="55cb4-150">NOTES</span></span>

## <span data-ttu-id="55cb4-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55cb4-151">RELATED LINKS</span></span>
