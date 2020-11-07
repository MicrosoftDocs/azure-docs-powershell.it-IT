---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: d31c80a2da8e705c2515283ca219d05484e3c3dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675644"
---
# <span data-ttu-id="73c45-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="73c45-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="73c45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73c45-102">SYNOPSIS</span></span>
<span data-ttu-id="73c45-103">Aggiorna le impostazioni per l'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="73c45-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="73c45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73c45-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73c45-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73c45-105">DESCRIPTION</span></span>
<span data-ttu-id="73c45-106">Il cmdlet **set-AzBatchApplication** modifica le impostazioni per l'applicazione batch Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="73c45-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="73c45-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73c45-107">EXAMPLES</span></span>

### <span data-ttu-id="73c45-108">Esempio 1: aggiornare un'applicazione in un account batch</span><span class="sxs-lookup"><span data-stu-id="73c45-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="73c45-109">Questo comando cambia se l'applicazione Litware nell'account ContosoBatch consente gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="73c45-109">This command changes whether the Litware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="73c45-110">Il comando non modifica la versione predefinita o il nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73c45-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="73c45-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73c45-111">PARAMETERS</span></span>

### <span data-ttu-id="73c45-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="73c45-112">-AccountName</span></span>
<span data-ttu-id="73c45-113">Specifica il nome dell'account batch per cui questo cmdlet modifica un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73c45-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="73c45-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="73c45-114">-AllowUpdates</span></span>
<span data-ttu-id="73c45-115">Specifica se i pacchetti all'interno dell'applicazione possono essere sovrascritti usando la stessa stringa di versione.</span><span class="sxs-lookup"><span data-stu-id="73c45-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c45-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="73c45-116">-ApplicationId</span></span>
<span data-ttu-id="73c45-117">Specifica l'ID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73c45-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="73c45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c45-118">-DefaultProfile</span></span>
<span data-ttu-id="73c45-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73c45-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73c45-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="73c45-120">-DefaultVersion</span></span>
<span data-ttu-id="73c45-121">Specifica il pacchetto da usare se un client richiede l'applicazione ma non specifica una versione.</span><span class="sxs-lookup"><span data-stu-id="73c45-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="73c45-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="73c45-122">-DisplayName</span></span>
<span data-ttu-id="73c45-123">Specifica il nome visualizzato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73c45-123">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="73c45-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c45-124">-ResourceGroupName</span></span>
<span data-ttu-id="73c45-125">Specifica il nome del gruppo di risorse che contiene l'account batch.</span><span class="sxs-lookup"><span data-stu-id="73c45-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="73c45-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c45-126">CommonParameters</span></span>
<span data-ttu-id="73c45-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c45-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c45-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c45-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c45-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73c45-129">INPUTS</span></span>

### <span data-ttu-id="73c45-130">System. String</span><span class="sxs-lookup"><span data-stu-id="73c45-130">System.String</span></span>

### <span data-ttu-id="73c45-131">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="73c45-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="73c45-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73c45-132">OUTPUTS</span></span>

### <span data-ttu-id="73c45-133">System. void</span><span class="sxs-lookup"><span data-stu-id="73c45-133">System.Void</span></span>

## <span data-ttu-id="73c45-134">Note</span><span class="sxs-lookup"><span data-stu-id="73c45-134">NOTES</span></span>

## <span data-ttu-id="73c45-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73c45-135">RELATED LINKS</span></span>

[<span data-ttu-id="73c45-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="73c45-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="73c45-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="73c45-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="73c45-138">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="73c45-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="73c45-139">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="73c45-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="73c45-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="73c45-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="73c45-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="73c45-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

