---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 313813bec61dac2f5b41f7ad2d36e5ee5ba1b44f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511195"
---
# <span data-ttu-id="92130-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="92130-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="92130-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92130-102">SYNOPSIS</span></span>
<span data-ttu-id="92130-103">Modifica l'ACL di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92130-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92130-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92130-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92130-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92130-105">DESCRIPTION</span></span>
<span data-ttu-id="92130-106">Il cmdlet **set-AzureRmDataLakeStoreItemAcl** modifica l'elenco di controllo di accesso (ACL) di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92130-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="92130-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92130-107">EXAMPLES</span></span>

### <span data-ttu-id="92130-108">Esempio 1: impostare l'ACL per un file e una cartella</span><span class="sxs-lookup"><span data-stu-id="92130-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="92130-109">Il primo comando ottiene l'ACL per la directory radice dell'account ContosoADL e lo archivia nella variabile $ACL.</span><span class="sxs-lookup"><span data-stu-id="92130-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="92130-110">Il secondo comando imposta l'ACL per il file Test.txt a quella in $ACL.</span><span class="sxs-lookup"><span data-stu-id="92130-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="92130-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92130-111">PARAMETERS</span></span>

### <span data-ttu-id="92130-112">-Account</span><span class="sxs-lookup"><span data-stu-id="92130-112">-Account</span></span>
<span data-ttu-id="92130-113">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92130-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="92130-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="92130-114">-Acl</span></span>
<span data-ttu-id="92130-115">Specifica un ACL per un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="92130-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92130-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92130-116">-DefaultProfile</span></span>
<span data-ttu-id="92130-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92130-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92130-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92130-118">-PassThru</span></span>
<span data-ttu-id="92130-119">Indica che deve essere restituito l'ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="92130-119">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="92130-120">-Path</span><span class="sxs-lookup"><span data-stu-id="92130-120">-Path</span></span>
<span data-ttu-id="92130-121">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="92130-121">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="92130-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="92130-122">-Confirm</span></span>
<span data-ttu-id="92130-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92130-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92130-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92130-124">-WhatIf</span></span>
<span data-ttu-id="92130-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92130-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92130-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92130-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92130-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92130-127">CommonParameters</span></span>
<span data-ttu-id="92130-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92130-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92130-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92130-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92130-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92130-130">INPUTS</span></span>

### <span data-ttu-id="92130-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="92130-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="92130-132">Il parametro "ACL" accetta il valore di tipo "DataLakeStoreItemAce []" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="92130-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="92130-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92130-133">OUTPUTS</span></span>

### <span data-ttu-id="92130-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="92130-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="92130-135">Se si specifica PassThru, verrà restituito l'elenco di voci ACL risultante.</span><span class="sxs-lookup"><span data-stu-id="92130-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="92130-136">Note</span><span class="sxs-lookup"><span data-stu-id="92130-136">NOTES</span></span>

## <span data-ttu-id="92130-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92130-137">RELATED LINKS</span></span>

