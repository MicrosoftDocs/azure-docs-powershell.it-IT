---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 15c516e1d54b6e706176ceb28a1974e848945c47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511716"
---
# <span data-ttu-id="faffe-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="faffe-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="faffe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="faffe-102">SYNOPSIS</span></span>
<span data-ttu-id="faffe-103">Consente di spostare o rinominare un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="faffe-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faffe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="faffe-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faffe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faffe-105">DESCRIPTION</span></span>
<span data-ttu-id="faffe-106">Il cmdlet **Move-AzureRmDataLakeStoreItem** sposta o rinomina un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="faffe-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="faffe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="faffe-107">EXAMPLES</span></span>

### <span data-ttu-id="faffe-108">Esempio 1: modificare e rinominare un elemento</span><span class="sxs-lookup"><span data-stu-id="faffe-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="faffe-109">Questo comando Rinomina l'elemento File.txt in RenamedFile.txt e lo sposta in una cartella diversa.</span><span class="sxs-lookup"><span data-stu-id="faffe-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="faffe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="faffe-110">PARAMETERS</span></span>

### <span data-ttu-id="faffe-111">-Account</span><span class="sxs-lookup"><span data-stu-id="faffe-111">-Account</span></span>
<span data-ttu-id="faffe-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="faffe-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="faffe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faffe-113">-DefaultProfile</span></span>
<span data-ttu-id="faffe-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="faffe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faffe-115">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="faffe-115">-Destination</span></span>
<span data-ttu-id="faffe-116">Specifica il percorso dello Store Data Lake a cui trasferire l'elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="faffe-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="faffe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="faffe-117">-Force</span></span>
<span data-ttu-id="faffe-118">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="faffe-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="faffe-119">-Path</span><span class="sxs-lookup"><span data-stu-id="faffe-119">-Path</span></span>
<span data-ttu-id="faffe-120">Specifica il percorso dello Store Data Lake dell'elemento da trasferire o rinominare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="faffe-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="faffe-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="faffe-121">-Confirm</span></span>
<span data-ttu-id="faffe-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faffe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faffe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faffe-123">-WhatIf</span></span>
<span data-ttu-id="faffe-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faffe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faffe-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faffe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faffe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faffe-126">CommonParameters</span></span>
<span data-ttu-id="faffe-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faffe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faffe-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faffe-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faffe-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="faffe-129">INPUTS</span></span>

### <span data-ttu-id="faffe-130">System. String</span><span class="sxs-lookup"><span data-stu-id="faffe-130">System.String</span></span>

### <span data-ttu-id="faffe-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="faffe-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="faffe-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="faffe-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="faffe-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="faffe-133">OUTPUTS</span></span>

### <span data-ttu-id="faffe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="faffe-134">System.String</span></span>
<span data-ttu-id="faffe-135">Percorso completo per il file o la cartella spostata.</span><span class="sxs-lookup"><span data-stu-id="faffe-135">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="faffe-136">Note</span><span class="sxs-lookup"><span data-stu-id="faffe-136">NOTES</span></span>

## <span data-ttu-id="faffe-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="faffe-137">RELATED LINKS</span></span>

[<span data-ttu-id="faffe-138">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="faffe-138">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="faffe-139">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="faffe-139">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="faffe-140">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="faffe-140">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="faffe-141">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="faffe-141">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="faffe-142">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="faffe-142">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="faffe-143">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="faffe-143">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


