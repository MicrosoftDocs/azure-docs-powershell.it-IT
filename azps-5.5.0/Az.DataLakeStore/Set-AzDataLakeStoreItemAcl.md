---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 8b3412acd7513718c8c34e3fc8bb10c5e33f11a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188583"
---
# <span data-ttu-id="422c8-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="422c8-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="422c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="422c8-102">SYNOPSIS</span></span>
<span data-ttu-id="422c8-103">Modifica l'ACL di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="422c8-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="422c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="422c8-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="422c8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="422c8-105">DESCRIPTION</span></span>
<span data-ttu-id="422c8-106">Il cmdlet **Set-AzDataLakeStoreItemAcl** modifica l'elenco di controllo di accesso (ACL) di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="422c8-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="422c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="422c8-107">EXAMPLES</span></span>

### <span data-ttu-id="422c8-108">Esempio 1: Impostare l'ACL per un file e una cartella</span><span class="sxs-lookup"><span data-stu-id="422c8-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="422c8-109">Il primo comando ottiene l'ACL per la directory radice dell'account ContosoADL e quindi lo archivia nella $ACL variabile.</span><span class="sxs-lookup"><span data-stu-id="422c8-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="422c8-110">Il secondo comando imposta l'ACL per il file Test.txt su quello della $ACL.</span><span class="sxs-lookup"><span data-stu-id="422c8-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="422c8-111">Esempio 2: Impostare l'ACL per la cartella in modo ricorsivo</span><span class="sxs-lookup"><span data-stu-id="422c8-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="422c8-112">Il primo comando ottiene l'ACL per la directory Folder1 dell'account ContosoADL e quindi lo archivia nella $ACL variabile.</span><span class="sxs-lookup"><span data-stu-id="422c8-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="422c8-113">Il secondo comando imposta l'ACL in modo ricorsivo su Cartella2 e le relative sotto directory e i relativi file su quello in $ACL.</span><span class="sxs-lookup"><span data-stu-id="422c8-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="422c8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="422c8-114">PARAMETERS</span></span>

### <span data-ttu-id="422c8-115">-Account</span><span class="sxs-lookup"><span data-stu-id="422c8-115">-Account</span></span>
<span data-ttu-id="422c8-116">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="422c8-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="422c8-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="422c8-117">-Acl</span></span>
<span data-ttu-id="422c8-118">Specifica un ACL per un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="422c8-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="422c8-119">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="422c8-119">-Concurrency</span></span>
<span data-ttu-id="422c8-120">Numero di file/directory elaborati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="422c8-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="422c8-121">Facoltativo: verrà selezionata un'impostazione predefinita ragionevole.</span><span class="sxs-lookup"><span data-stu-id="422c8-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="422c8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="422c8-122">-DefaultProfile</span></span>
<span data-ttu-id="422c8-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="422c8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="422c8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="422c8-124">-PassThru</span></span>
<span data-ttu-id="422c8-125">Indica che deve essere restituito l'ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="422c8-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="422c8-126">-Path</span><span class="sxs-lookup"><span data-stu-id="422c8-126">-Path</span></span>
<span data-ttu-id="422c8-127">Specifica il percorso Data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="422c8-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="422c8-128">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="422c8-128">-Recurse</span></span>
<span data-ttu-id="422c8-129">Indica l'ACL da impostare in modo ricorsivo per le sottodirectory e i file figlio</span><span class="sxs-lookup"><span data-stu-id="422c8-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="422c8-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="422c8-130">-ShowProgress</span></span>
<span data-ttu-id="422c8-131">Se viene superato, viene visualizzato lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="422c8-131">If passed then progress status is showed.</span></span> <span data-ttu-id="422c8-132">Applicabile solo quando il set di Acl ricorsivo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="422c8-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="422c8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="422c8-133">-Confirm</span></span>
<span data-ttu-id="422c8-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="422c8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="422c8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="422c8-135">-WhatIf</span></span>
<span data-ttu-id="422c8-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="422c8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="422c8-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="422c8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="422c8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="422c8-138">CommonParameters</span></span>
<span data-ttu-id="422c8-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="422c8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="422c8-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="422c8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="422c8-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="422c8-141">INPUTS</span></span>

### <span data-ttu-id="422c8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="422c8-142">System.String</span></span>

### <span data-ttu-id="422c8-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="422c8-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="422c8-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="422c8-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="422c8-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="422c8-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="422c8-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="422c8-146">System.Int32</span></span>

## <span data-ttu-id="422c8-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="422c8-147">OUTPUTS</span></span>

### <span data-ttu-id="422c8-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="422c8-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="422c8-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="422c8-149">NOTES</span></span>

## <span data-ttu-id="422c8-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="422c8-150">RELATED LINKS</span></span>
