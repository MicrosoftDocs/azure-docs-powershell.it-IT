---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 17653793-3CE1-465F-87F7-20B4B8F56193
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplicationPackage.md
ms.openlocfilehash: e5e289679327b0376530f01f91310cf211465e48
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205339"
---
# <span data-ttu-id="fc0e9-101">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fc0e9-101">Get-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="fc0e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc0e9-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0e9-103">Ottiene informazioni su un pacchetto dell'applicazione in un account batch.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-103">Gets information about an application package in a Batch account.</span></span>

## <span data-ttu-id="fc0e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc0e9-104">SYNTAX</span></span>

```
Get-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-ApplicationVersion] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc0e9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc0e9-105">DESCRIPTION</span></span>
<span data-ttu-id="fc0e9-106">Il cmdlet **Get-AzBatchApplicationPackage** ottiene informazioni su un pacchetto dell'applicazione in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-106">The **Get-AzBatchApplicationPackage** cmdlet gets information about an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="fc0e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc0e9-107">EXAMPLES</span></span>

### <span data-ttu-id="fc0e9-108">Esempio 1: Ottenere i dettagli di un pacchetto dell'applicazione in un account Batch</span><span class="sxs-lookup"><span data-stu-id="fc0e9-108">Example 1: Get details of an application package in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0"
Format             : zip
State              : Active
Version            : 1.0
LastActivationTime : 13/05/2016 4:03:24 AM
StorageUrl         : https://contosobatch.blob.core.windows.net/app-test
StorageUrlExpiry   : 13/05/2016 8:04:44 AM
Id                 : litware
```

<span data-ttu-id="fc0e9-109">Questo comando recupera i dettagli della versione 1.0 del pacchetto Litware.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-109">This command gets the details of version 1.0 of the Litware package.</span></span>

## <span data-ttu-id="fc0e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc0e9-110">PARAMETERS</span></span>

### <span data-ttu-id="fc0e9-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc0e9-111">-AccountName</span></span>
<span data-ttu-id="fc0e9-112">Specifica il nome dell'account batch da cui il cmdlet riceve informazioni.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-112">Specifies the name of the Batch account from which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="fc0e9-113">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="fc0e9-113">-ApplicationName</span></span>
<span data-ttu-id="fc0e9-114">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-114">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0e9-115">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="fc0e9-115">-ApplicationVersion</span></span>
<span data-ttu-id="fc0e9-116">Specifica la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-116">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0e9-117">-DefaultProfile</span></span>
<span data-ttu-id="fc0e9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc0e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc0e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc0e9-120">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-120">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="fc0e9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0e9-121">CommonParameters</span></span>
<span data-ttu-id="fc0e9-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0e9-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc0e9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0e9-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc0e9-124">INPUTS</span></span>

### <span data-ttu-id="fc0e9-125">System.String</span><span class="sxs-lookup"><span data-stu-id="fc0e9-125">System.String</span></span>

## <span data-ttu-id="fc0e9-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc0e9-126">OUTPUTS</span></span>

### <span data-ttu-id="fc0e9-127">Microsoft.Azure.Commands.Batch. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fc0e9-127">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="fc0e9-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc0e9-128">NOTES</span></span>

## <span data-ttu-id="fc0e9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc0e9-129">RELATED LINKS</span></span>

[<span data-ttu-id="fc0e9-130">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fc0e9-130">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="fc0e9-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fc0e9-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="fc0e9-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fc0e9-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="fc0e9-133">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fc0e9-133">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="fc0e9-134">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="fc0e9-134">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="fc0e9-135">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="fc0e9-135">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


