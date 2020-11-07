---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
ms.openlocfilehash: d94b5e21913112d9e7d29a3e4012909dd5c9c3c0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866412"
---
# <span data-ttu-id="83b65-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="83b65-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="83b65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83b65-102">SYNOPSIS</span></span>
<span data-ttu-id="83b65-103">Abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="83b65-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83b65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83b65-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b65-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83b65-105">DESCRIPTION</span></span>
<span data-ttu-id="83b65-106">Il cmdlet **Enable-AzureStorageDeleteRetentionPolicy** consente di eliminare i criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="83b65-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="83b65-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83b65-107">EXAMPLES</span></span>

### <span data-ttu-id="83b65-108">Esempio 1: abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="83b65-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="83b65-109">Questo comando consente di eliminare i criteri di conservazione per il servizio BLOB e di impostare i giorni di conservazione BLOB eliminati su 3.</span><span class="sxs-lookup"><span data-stu-id="83b65-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="83b65-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83b65-110">PARAMETERS</span></span>

### <span data-ttu-id="83b65-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="83b65-111">-Context</span></span>
<span data-ttu-id="83b65-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="83b65-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83b65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b65-113">-DefaultProfile</span></span>
<span data-ttu-id="83b65-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83b65-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b65-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83b65-115">-PassThru</span></span>
<span data-ttu-id="83b65-116">Visualizza DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="83b65-116">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b65-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="83b65-117">-RetentionDays</span></span>
<span data-ttu-id="83b65-118">Imposta il numero di giorni di conservazione per DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="83b65-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b65-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83b65-119">-Confirm</span></span>
<span data-ttu-id="83b65-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b65-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b65-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b65-121">-WhatIf</span></span>
<span data-ttu-id="83b65-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b65-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b65-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b65-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b65-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b65-124">CommonParameters</span></span>
<span data-ttu-id="83b65-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b65-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b65-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b65-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b65-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83b65-127">INPUTS</span></span>

### <span data-ttu-id="83b65-128">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="83b65-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="83b65-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83b65-129">OUTPUTS</span></span>

### <span data-ttu-id="83b65-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="83b65-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="83b65-131">Note</span><span class="sxs-lookup"><span data-stu-id="83b65-131">NOTES</span></span>

## <span data-ttu-id="83b65-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83b65-132">RELATED LINKS</span></span>
