---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200540"
---
# <span data-ttu-id="24a88-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="24a88-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="24a88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24a88-102">SYNOPSIS</span></span>
<span data-ttu-id="24a88-103">Elimina un'applicazione da un account batch.</span><span class="sxs-lookup"><span data-stu-id="24a88-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="24a88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24a88-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24a88-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24a88-105">DESCRIPTION</span></span>
<span data-ttu-id="24a88-106">Il cmdlet **Remove-AzBatchApplication** Elimina un'applicazione da un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="24a88-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="24a88-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24a88-107">EXAMPLES</span></span>

### <span data-ttu-id="24a88-108">Esempio 1: eliminare un'applicazione da un account batch</span><span class="sxs-lookup"><span data-stu-id="24a88-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="24a88-109">Questo comando Elimina l'applicazione Litware dall'account ContosoBatch.</span><span class="sxs-lookup"><span data-stu-id="24a88-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="24a88-110">Il comando non riesce se l'applicazione contiene pacchetti.</span><span class="sxs-lookup"><span data-stu-id="24a88-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="24a88-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24a88-111">PARAMETERS</span></span>

### <span data-ttu-id="24a88-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24a88-112">-AccountName</span></span>
<span data-ttu-id="24a88-113">Specifica il nome dell'account batch da cui questo cmdlet rimuove un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24a88-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="24a88-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="24a88-114">-ApplicationName</span></span>
<span data-ttu-id="24a88-115">Specifica il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24a88-115">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="24a88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a88-116">-DefaultProfile</span></span>
<span data-ttu-id="24a88-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24a88-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a88-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a88-118">-ResourceGroupName</span></span>
<span data-ttu-id="24a88-119">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="24a88-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="24a88-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a88-120">CommonParameters</span></span>
<span data-ttu-id="24a88-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24a88-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a88-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24a88-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a88-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24a88-123">INPUTS</span></span>

### <span data-ttu-id="24a88-124">System. String</span><span class="sxs-lookup"><span data-stu-id="24a88-124">System.String</span></span>

## <span data-ttu-id="24a88-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24a88-125">OUTPUTS</span></span>

### <span data-ttu-id="24a88-126">System. void</span><span class="sxs-lookup"><span data-stu-id="24a88-126">System.Void</span></span>

## <span data-ttu-id="24a88-127">Note</span><span class="sxs-lookup"><span data-stu-id="24a88-127">NOTES</span></span>

## <span data-ttu-id="24a88-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24a88-128">RELATED LINKS</span></span>

[<span data-ttu-id="24a88-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="24a88-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="24a88-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="24a88-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="24a88-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="24a88-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="24a88-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="24a88-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="24a88-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="24a88-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="24a88-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="24a88-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


