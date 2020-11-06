---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 7d8552ccc2c293f33c71402043a28bfad32ceeeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509328"
---
# <span data-ttu-id="b0aea-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b0aea-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="b0aea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0aea-102">SYNOPSIS</span></span>
<span data-ttu-id="b0aea-103">Elimina un record pacchetto dell'applicazione e il file binario.</span><span class="sxs-lookup"><span data-stu-id="b0aea-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0aea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0aea-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0aea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0aea-105">DESCRIPTION</span></span>
<span data-ttu-id="b0aea-106">Il cmdlet **Remove-AzureRmBatchApplicationPackage** Elimina un record del pacchetto dell'applicazione e il file binario da un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0aea-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="b0aea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0aea-107">EXAMPLES</span></span>

### <span data-ttu-id="b0aea-108">Esempio 1: eliminare un pacchetto di applicazione da un account batch</span><span class="sxs-lookup"><span data-stu-id="b0aea-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="b0aea-109">Questo comando Elimina la versione 1,0 dell'applicazione Litware dall'account ContosoBatchGroup.</span><span class="sxs-lookup"><span data-stu-id="b0aea-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="b0aea-110">Il comando Elimina sia il record del pacchetto che il BLOB che contengono il file binario del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="b0aea-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="b0aea-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0aea-111">PARAMETERS</span></span>

### <span data-ttu-id="b0aea-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0aea-112">-AccountName</span></span>
<span data-ttu-id="b0aea-113">Specifica il nome dell'account batch da cui questo cmdlet elimina un pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0aea-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0aea-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b0aea-114">-ApplicationId</span></span>
<span data-ttu-id="b0aea-115">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0aea-115">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0aea-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="b0aea-116">-ApplicationVersion</span></span>
<span data-ttu-id="b0aea-117">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0aea-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0aea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0aea-118">-DefaultProfile</span></span>
<span data-ttu-id="b0aea-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0aea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0aea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0aea-120">-ResourceGroupName</span></span>
<span data-ttu-id="b0aea-121">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="b0aea-121">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0aea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0aea-122">CommonParameters</span></span>
<span data-ttu-id="b0aea-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0aea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0aea-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0aea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0aea-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0aea-125">INPUTS</span></span>

### <span data-ttu-id="b0aea-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b0aea-126">System.String</span></span>

## <span data-ttu-id="b0aea-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0aea-127">OUTPUTS</span></span>

### <span data-ttu-id="b0aea-128">System. void</span><span class="sxs-lookup"><span data-stu-id="b0aea-128">System.Void</span></span>

## <span data-ttu-id="b0aea-129">Note</span><span class="sxs-lookup"><span data-stu-id="b0aea-129">NOTES</span></span>

## <span data-ttu-id="b0aea-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0aea-130">RELATED LINKS</span></span>

[<span data-ttu-id="b0aea-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b0aea-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="b0aea-132">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b0aea-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b0aea-133">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b0aea-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="b0aea-134">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b0aea-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b0aea-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b0aea-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="b0aea-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b0aea-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


