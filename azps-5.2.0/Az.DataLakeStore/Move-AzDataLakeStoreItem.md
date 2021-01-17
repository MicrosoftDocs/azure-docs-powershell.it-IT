---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347503"
---
# <span data-ttu-id="1253d-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1253d-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="1253d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1253d-102">SYNOPSIS</span></span>
<span data-ttu-id="1253d-103">Consente di spostare o rinominare un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1253d-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1253d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1253d-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1253d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1253d-105">DESCRIPTION</span></span>
<span data-ttu-id="1253d-106">Il cmdlet **Move-AzDataLakeStoreItem** sposta o rinomina un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1253d-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1253d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1253d-107">EXAMPLES</span></span>

### <span data-ttu-id="1253d-108">Esempio 1: modificare e rinominare un elemento</span><span class="sxs-lookup"><span data-stu-id="1253d-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="1253d-109">Questo comando Rinomina l'elemento File.txt in RenamedFile.txt e lo sposta in una cartella diversa.</span><span class="sxs-lookup"><span data-stu-id="1253d-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="1253d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1253d-110">PARAMETERS</span></span>

### <span data-ttu-id="1253d-111">-Account</span><span class="sxs-lookup"><span data-stu-id="1253d-111">-Account</span></span>
<span data-ttu-id="1253d-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1253d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1253d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1253d-113">-DefaultProfile</span></span>
<span data-ttu-id="1253d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1253d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1253d-115">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="1253d-115">-Destination</span></span>
<span data-ttu-id="1253d-116">Specifica il percorso dello Store Data Lake a cui trasferire l'elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="1253d-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1253d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1253d-117">-Force</span></span>
<span data-ttu-id="1253d-118">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="1253d-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1253d-119">-Path</span><span class="sxs-lookup"><span data-stu-id="1253d-119">-Path</span></span>
<span data-ttu-id="1253d-120">Specifica il percorso dello Store Data Lake dell'elemento da trasferire o rinominare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="1253d-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1253d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1253d-121">-Confirm</span></span>
<span data-ttu-id="1253d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1253d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1253d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1253d-123">-WhatIf</span></span>
<span data-ttu-id="1253d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1253d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1253d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1253d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1253d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1253d-126">CommonParameters</span></span>
<span data-ttu-id="1253d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1253d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1253d-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1253d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1253d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1253d-129">INPUTS</span></span>

### <span data-ttu-id="1253d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1253d-130">System.String</span></span>

### <span data-ttu-id="1253d-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1253d-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1253d-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1253d-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1253d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1253d-133">OUTPUTS</span></span>

### <span data-ttu-id="1253d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1253d-134">System.String</span></span>

## <span data-ttu-id="1253d-135">Note</span><span class="sxs-lookup"><span data-stu-id="1253d-135">NOTES</span></span>

## <span data-ttu-id="1253d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1253d-136">RELATED LINKS</span></span>

[<span data-ttu-id="1253d-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1253d-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="1253d-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1253d-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="1253d-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1253d-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="1253d-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1253d-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="1253d-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1253d-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="1253d-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1253d-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


