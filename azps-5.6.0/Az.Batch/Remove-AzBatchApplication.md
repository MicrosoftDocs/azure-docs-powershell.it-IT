---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: ebe28df5c69ce966a9d05d2e34cd9e66693d7f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992947"
---
# <span data-ttu-id="76d89-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="76d89-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="76d89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d89-102">SYNOPSIS</span></span>
<span data-ttu-id="76d89-103">Elimina un'applicazione da un account batch.</span><span class="sxs-lookup"><span data-stu-id="76d89-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="76d89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76d89-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76d89-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="76d89-105">DESCRIPTION</span></span>
<span data-ttu-id="76d89-106">Il cmdlet **Remove-AzBatchApplication** elimina un'applicazione da un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="76d89-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="76d89-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76d89-107">EXAMPLES</span></span>

### <span data-ttu-id="76d89-108">Esempio 1: Eliminare un'applicazione da un account batch</span><span class="sxs-lookup"><span data-stu-id="76d89-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="76d89-109">Questo comando elimina l'applicazione Litware dall'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="76d89-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="76d89-110">Il comando non riesce se l'applicazione contiene pacchetti.</span><span class="sxs-lookup"><span data-stu-id="76d89-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="76d89-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76d89-111">PARAMETERS</span></span>

### <span data-ttu-id="76d89-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76d89-112">-AccountName</span></span>
<span data-ttu-id="76d89-113">Specifica il nome dell'account batch da cui questo cmdlet rimuove un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="76d89-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="76d89-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="76d89-114">-ApplicationName</span></span>
<span data-ttu-id="76d89-115">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="76d89-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="76d89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d89-116">-DefaultProfile</span></span>
<span data-ttu-id="76d89-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76d89-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76d89-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d89-118">-ResourceGroupName</span></span>
<span data-ttu-id="76d89-119">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="76d89-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="76d89-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d89-120">CommonParameters</span></span>
<span data-ttu-id="76d89-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d89-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d89-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76d89-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d89-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="76d89-123">INPUTS</span></span>

### <span data-ttu-id="76d89-124">System.String</span><span class="sxs-lookup"><span data-stu-id="76d89-124">System.String</span></span>

## <span data-ttu-id="76d89-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76d89-125">OUTPUTS</span></span>

### <span data-ttu-id="76d89-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="76d89-126">System.Void</span></span>

## <span data-ttu-id="76d89-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="76d89-127">NOTES</span></span>

## <span data-ttu-id="76d89-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76d89-128">RELATED LINKS</span></span>

[<span data-ttu-id="76d89-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="76d89-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="76d89-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="76d89-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="76d89-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="76d89-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="76d89-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="76d89-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="76d89-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="76d89-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="76d89-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="76d89-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


