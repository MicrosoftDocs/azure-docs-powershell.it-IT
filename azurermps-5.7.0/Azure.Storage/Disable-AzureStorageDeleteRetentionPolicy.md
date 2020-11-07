---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685644"
---
# <span data-ttu-id="48f3d-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="48f3d-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="48f3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="48f3d-103">Disabilitare i criteri di conservazione Elimina per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="48f3d-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48f3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48f3d-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48f3d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48f3d-105">DESCRIPTION</span></span>
<span data-ttu-id="48f3d-106">Il cmdlet **Disable-AzureStorageDeleteRetentionPolicy Disabilita** l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="48f3d-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="48f3d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48f3d-107">EXAMPLES</span></span>

### <span data-ttu-id="48f3d-108">Esempio 1: disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="48f3d-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="48f3d-109">Questo comando Disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="48f3d-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="48f3d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48f3d-110">PARAMETERS</span></span>

### <span data-ttu-id="48f3d-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="48f3d-111">-Context</span></span>
<span data-ttu-id="48f3d-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="48f3d-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="48f3d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48f3d-113">-PassThru</span></span>
<span data-ttu-id="48f3d-114">Visualizza DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="48f3d-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="48f3d-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="48f3d-115">-Confirm</span></span>
<span data-ttu-id="48f3d-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48f3d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48f3d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f3d-117">-WhatIf</span></span>
<span data-ttu-id="48f3d-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48f3d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48f3d-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48f3d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48f3d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f3d-120">CommonParameters</span></span>
<span data-ttu-id="48f3d-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48f3d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f3d-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f3d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f3d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48f3d-123">INPUTS</span></span>

### <span data-ttu-id="48f3d-124">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="48f3d-124">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="48f3d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48f3d-125">OUTPUTS</span></span>

### <span data-ttu-id="48f3d-126">Microsoft. WindowsAzure. Commands. storage. Model. resourcemode. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="48f3d-126">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceMode.PSSeriviceProperties</span></span>

## <span data-ttu-id="48f3d-127">Note</span><span class="sxs-lookup"><span data-stu-id="48f3d-127">NOTES</span></span>

## <span data-ttu-id="48f3d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48f3d-128">RELATED LINKS</span></span>

