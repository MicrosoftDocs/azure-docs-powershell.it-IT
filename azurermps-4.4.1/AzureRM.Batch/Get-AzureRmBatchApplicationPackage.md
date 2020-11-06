---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: f260af1bc26d9cf921a26e4f08c3c4feab4b79c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516284"
---
# <span data-ttu-id="eb3af-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="eb3af-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="eb3af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb3af-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3af-103">Ottiene le informazioni su un pacchetto di applicazione in un account batch.</span><span class="sxs-lookup"><span data-stu-id="eb3af-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb3af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb3af-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb3af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb3af-105">DESCRIPTION</span></span>
<span data-ttu-id="eb3af-106">Il cmdlet **Get-AzureRmBatchApplicationPackage** ottiene le informazioni su un pacchetto dell'applicazione in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="eb3af-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="eb3af-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb3af-107">EXAMPLES</span></span>

### <span data-ttu-id="eb3af-108">Esempio 1: ottenere informazioni dettagliate su un pacchetto di applicazione in un account batch</span><span class="sxs-lookup"><span data-stu-id="eb3af-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="eb3af-109">Questo comando consente di ottenere i dettagli della versione 1,0 del pacchetto Litware.</span><span class="sxs-lookup"><span data-stu-id="eb3af-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="eb3af-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb3af-110">PARAMETERS</span></span>

### <span data-ttu-id="eb3af-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb3af-111">-AccountName</span></span>
<span data-ttu-id="eb3af-112">Specifica il nome dell'account batch da cui questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="eb3af-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="eb3af-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="eb3af-113">-ApplicationId</span></span>
<span data-ttu-id="eb3af-114">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb3af-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="eb3af-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="eb3af-115">-ApplicationVersion</span></span>
<span data-ttu-id="eb3af-116">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb3af-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="eb3af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb3af-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb3af-118">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="eb3af-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="eb3af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3af-119">-DefaultProfile</span></span>
<span data-ttu-id="eb3af-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb3af-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb3af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3af-121">CommonParameters</span></span>
<span data-ttu-id="eb3af-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb3af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3af-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb3af-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3af-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb3af-124">INPUTS</span></span>

## <span data-ttu-id="eb3af-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb3af-125">OUTPUTS</span></span>

### <span data-ttu-id="eb3af-126">Microsoft.Azure.Commands.Batch. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="eb3af-126">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="eb3af-127">Note</span><span class="sxs-lookup"><span data-stu-id="eb3af-127">NOTES</span></span>

## <span data-ttu-id="eb3af-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb3af-128">RELATED LINKS</span></span>

[<span data-ttu-id="eb3af-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="eb3af-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="eb3af-130">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="eb3af-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="eb3af-131">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="eb3af-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="eb3af-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="eb3af-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="eb3af-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="eb3af-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="eb3af-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="eb3af-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


