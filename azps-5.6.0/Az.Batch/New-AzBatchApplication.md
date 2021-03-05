---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: e22c1ef6a95fafe21f0fd10a47a67098976395e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966749"
---
# <span data-ttu-id="d7a2e-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d7a2e-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="d7a2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a2e-103">Aggiunge un'applicazione all'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="d7a2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7a2e-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7a2e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d7a2e-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a2e-106">Il cmdlet **New-AzBatchApplication** aggiunge un'applicazione all'account batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="d7a2e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7a2e-107">EXAMPLES</span></span>

### <span data-ttu-id="d7a2e-108">Esempio 1: Aggiungere un'applicazione vuota a un account batch</span><span class="sxs-lookup"><span data-stu-id="d7a2e-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="d7a2e-109">Questo comando crea l'applicazione Litware nell'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="d7a2e-110">L'applicazione inizialmente non contiene pacchetti.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="d7a2e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7a2e-111">PARAMETERS</span></span>

### <span data-ttu-id="d7a2e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7a2e-112">-AccountName</span></span>
<span data-ttu-id="d7a2e-113">Specifica il nome dell'account batch a cui questo cmdlet aggiunge un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="d7a2e-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="d7a2e-114">-AllowUpdates</span></span>
<span data-ttu-id="d7a2e-115">Specifica se i pacchetti all'interno dell'applicazione possono essere sovrascritti usando la stessa stringa di versione.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7a2e-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="d7a2e-116">-ApplicationName</span></span>
<span data-ttu-id="d7a2e-117">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="d7a2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a2e-118">-DefaultProfile</span></span>
<span data-ttu-id="d7a2e-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7a2e-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d7a2e-120">-DisplayName</span></span>
<span data-ttu-id="d7a2e-121">Specifica il nome visualizzato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-121">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7a2e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a2e-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7a2e-123">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d7a2e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a2e-124">CommonParameters</span></span>
<span data-ttu-id="d7a2e-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a2e-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d7a2e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a2e-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="d7a2e-127">INPUTS</span></span>

### <span data-ttu-id="d7a2e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d7a2e-128">System.String</span></span>

### <span data-ttu-id="d7a2e-129">System.Nullable'1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d7a2e-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d7a2e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7a2e-130">OUTPUTS</span></span>

### <span data-ttu-id="d7a2e-131">Microsoft.Azure.Commands.Batch. Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="d7a2e-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="d7a2e-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="d7a2e-132">NOTES</span></span>

## <span data-ttu-id="d7a2e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7a2e-133">RELATED LINKS</span></span>

[<span data-ttu-id="d7a2e-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d7a2e-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="d7a2e-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d7a2e-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="d7a2e-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d7a2e-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="d7a2e-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d7a2e-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="d7a2e-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d7a2e-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="d7a2e-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d7a2e-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


