---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510212"
---
# <span data-ttu-id="21b10-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="21b10-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="21b10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21b10-102">SYNOPSIS</span></span>
<span data-ttu-id="21b10-103">Abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="21b10-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21b10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21b10-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21b10-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21b10-105">DESCRIPTION</span></span>
<span data-ttu-id="21b10-106">Il cmdlet **Enable-AzureStorageDeleteRetentionPolicy** consente di eliminare i criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="21b10-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="21b10-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21b10-107">EXAMPLES</span></span>

### <span data-ttu-id="21b10-108">Esempio 1: abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="21b10-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="21b10-109">Questo comando consente di eliminare i criteri di conservazione per il servizio BLOB e di impostare i giorni di conservazione BLOB eliminati su 3.</span><span class="sxs-lookup"><span data-stu-id="21b10-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="21b10-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21b10-110">PARAMETERS</span></span>

### <span data-ttu-id="21b10-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="21b10-111">-Context</span></span>
<span data-ttu-id="21b10-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="21b10-112">Azure Storage Context Object</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21b10-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21b10-113">-PassThru</span></span>
<span data-ttu-id="21b10-114">Visualizza DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="21b10-114">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b10-115">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="21b10-115">-RetentionDays</span></span>
<span data-ttu-id="21b10-116">Imposta il numero di giorni di conservazione per DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="21b10-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b10-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21b10-117">-Confirm</span></span>
<span data-ttu-id="21b10-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21b10-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b10-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21b10-119">-WhatIf</span></span>
<span data-ttu-id="21b10-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21b10-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21b10-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21b10-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b10-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b10-122">CommonParameters</span></span>
<span data-ttu-id="21b10-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21b10-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b10-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b10-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b10-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21b10-125">INPUTS</span></span>

### <span data-ttu-id="21b10-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="21b10-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="21b10-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21b10-127">OUTPUTS</span></span>

### <span data-ttu-id="21b10-128">Microsoft. WindowsAzure. storage. Shared. Protocol. DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="21b10-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="21b10-129">Note</span><span class="sxs-lookup"><span data-stu-id="21b10-129">NOTES</span></span>

## <span data-ttu-id="21b10-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21b10-130">RELATED LINKS</span></span>

