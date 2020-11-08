---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032657"
---
# <span data-ttu-id="595c4-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="595c4-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="595c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="595c4-102">SYNOPSIS</span></span>
<span data-ttu-id="595c4-103">Elimina un'applicazione da un account batch.</span><span class="sxs-lookup"><span data-stu-id="595c4-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="595c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="595c4-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="595c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="595c4-105">DESCRIPTION</span></span>
<span data-ttu-id="595c4-106">Il cmdlet **Remove-AzBatchApplication** Elimina un'applicazione da un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="595c4-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="595c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="595c4-107">EXAMPLES</span></span>

### <span data-ttu-id="595c4-108">Esempio 1: eliminare un'applicazione da un account batch</span><span class="sxs-lookup"><span data-stu-id="595c4-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="595c4-109">Questo comando Elimina l'applicazione Litware dall'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="595c4-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="595c4-110">Il comando non riesce se l'applicazione contiene pacchetti.</span><span class="sxs-lookup"><span data-stu-id="595c4-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="595c4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="595c4-111">PARAMETERS</span></span>

### <span data-ttu-id="595c4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="595c4-112">-AccountName</span></span>
<span data-ttu-id="595c4-113">Specifica il nome dell'account batch da cui questo cmdlet rimuove un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="595c4-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="595c4-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="595c4-114">-ApplicationName</span></span>
<span data-ttu-id="595c4-115">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="595c4-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="595c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595c4-116">-DefaultProfile</span></span>
<span data-ttu-id="595c4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="595c4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="595c4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595c4-118">-ResourceGroupName</span></span>
<span data-ttu-id="595c4-119">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="595c4-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="595c4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595c4-120">CommonParameters</span></span>
<span data-ttu-id="595c4-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="595c4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595c4-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="595c4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595c4-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="595c4-123">INPUTS</span></span>

### <span data-ttu-id="595c4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="595c4-124">System.String</span></span>

## <span data-ttu-id="595c4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="595c4-125">OUTPUTS</span></span>

### <span data-ttu-id="595c4-126">System. void</span><span class="sxs-lookup"><span data-stu-id="595c4-126">System.Void</span></span>

## <span data-ttu-id="595c4-127">Note</span><span class="sxs-lookup"><span data-stu-id="595c4-127">NOTES</span></span>

## <span data-ttu-id="595c4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="595c4-128">RELATED LINKS</span></span>

[<span data-ttu-id="595c4-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="595c4-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="595c4-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="595c4-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="595c4-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="595c4-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="595c4-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="595c4-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="595c4-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="595c4-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="595c4-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="595c4-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


