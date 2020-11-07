---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: 0cbcc49f4b37b150b783467f45dcc7d4d7e53f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675662"
---
# <span data-ttu-id="7b3c0-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7b3c0-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="7b3c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3c0-103">Ottiene le informazioni su un pacchetto di applicazione in un account batch.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="7b3c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b3c0-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b3c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b3c0-105">DESCRIPTION</span></span>
<span data-ttu-id="7b3c0-106">Il cmdlet **Get-AzBatchApplicationPackage** ottiene le informazioni su un pacchetto dell'applicazione in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="7b3c0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b3c0-107">EXAMPLES</span></span>

### <span data-ttu-id="7b3c0-108">Esempio 1: ottenere informazioni dettagliate su un pacchetto di applicazione in un account batch</span><span class="sxs-lookup"><span data-stu-id="7b3c0-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="7b3c0-109">Questo comando consente di ottenere i dettagli della versione 1,0 del pacchetto Litware.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="7b3c0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b3c0-110">PARAMETERS</span></span>

### <span data-ttu-id="7b3c0-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7b3c0-111">-AccountName</span></span>
<span data-ttu-id="7b3c0-112">Specifica il nome dell'account batch da cui questo cmdlet ottiene le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="7b3c0-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7b3c0-113">-ApplicationId</span></span>
<span data-ttu-id="7b3c0-114">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="7b3c0-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="7b3c0-115">-ApplicationVersion</span></span>
<span data-ttu-id="7b3c0-116">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-116">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="7b3c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3c0-117">-DefaultProfile</span></span>
<span data-ttu-id="7b3c0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b3c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="7b3c0-120">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="7b3c0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3c0-121">CommonParameters</span></span>
<span data-ttu-id="7b3c0-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3c0-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b3c0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3c0-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b3c0-124">INPUTS</span></span>

### <span data-ttu-id="7b3c0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7b3c0-125">System.String</span></span>

## <span data-ttu-id="7b3c0-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b3c0-126">OUTPUTS</span></span>

### <span data-ttu-id="7b3c0-127">Microsoft.Azure.Commands.Batch. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7b3c0-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="7b3c0-128">Note</span><span class="sxs-lookup"><span data-stu-id="7b3c0-128">NOTES</span></span>

## <span data-ttu-id="7b3c0-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b3c0-129">RELATED LINKS</span></span>

[<span data-ttu-id="7b3c0-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7b3c0-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="7b3c0-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7b3c0-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="7b3c0-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7b3c0-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="7b3c0-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7b3c0-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="7b3c0-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7b3c0-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="7b3c0-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7b3c0-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


