---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 609c7e161b131d80f9b41355f13ced8636a591e8
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93522174"
---
# <span data-ttu-id="c0bc4-101">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c0bc4-101">Get-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="c0bc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="c0bc4-103">Ottiene le informazioni su un pacchetto di applicazione in un account batch.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-103">Gets information about an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0bc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0bc4-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0bc4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0bc4-105">DESCRIPTION</span></span>
<span data-ttu-id="c0bc4-106">Il cmdlet **Get-AzureRmBatchApplicationPackage** ottiene le informazioni su un pacchetto dell'applicazione in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-106">The **Get-AzureRmBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="c0bc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0bc4-107">EXAMPLES</span></span>

### <span data-ttu-id="c0bc4-108">Esempio 1: ottenere informazioni dettagliate su un pacchetto di applicazione in un account batch</span><span class="sxs-lookup"><span data-stu-id="c0bc4-108">Example 1: Get details of an application package in a Batch account</span></span>
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

<span data-ttu-id="c0bc4-109">Questo comando consente di ottenere i dettagli della versione 1,0 del pacchetto Litware.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="c0bc4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0bc4-110">PARAMETERS</span></span>

### <span data-ttu-id="c0bc4-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0bc4-111">-AccountName</span></span>
<span data-ttu-id="c0bc4-112">Specifica il nome dell'account batch da cui questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0bc4-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c0bc4-113">-ApplicationId</span></span>
<span data-ttu-id="c0bc4-114">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-114">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0bc4-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="c0bc4-115">-ApplicationVersion</span></span>
<span data-ttu-id="c0bc4-116">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-116">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0bc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0bc4-117">-DefaultProfile</span></span>
<span data-ttu-id="c0bc4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0bc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0bc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0bc4-120">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-120">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0bc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0bc4-121">CommonParameters</span></span>
<span data-ttu-id="c0bc4-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0bc4-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0bc4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0bc4-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0bc4-124">INPUTS</span></span>

### <span data-ttu-id="c0bc4-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c0bc4-125">None</span></span>
<span data-ttu-id="c0bc4-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c0bc4-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c0bc4-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0bc4-127">OUTPUTS</span></span>

### <span data-ttu-id="c0bc4-128">Microsoft.Azure.Commands.Batch. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c0bc4-128">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="c0bc4-129">Note</span><span class="sxs-lookup"><span data-stu-id="c0bc4-129">NOTES</span></span>

## <span data-ttu-id="c0bc4-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0bc4-130">RELATED LINKS</span></span>

[<span data-ttu-id="c0bc4-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c0bc4-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="c0bc4-132">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c0bc4-132">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="c0bc4-133">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c0bc4-133">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c0bc4-134">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c0bc4-134">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="c0bc4-135">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c0bc4-135">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c0bc4-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c0bc4-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


