---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: e9825c0efe0f54788cb074c862d51b747c6fbb9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676652"
---
# <span data-ttu-id="46c0c-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46c0c-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="46c0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="46c0c-103">Abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="46c0c-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="46c0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46c0c-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46c0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46c0c-105">DESCRIPTION</span></span>
<span data-ttu-id="46c0c-106">Il cmdlet **Enable-AzStorageDeleteRetentionPolicy** consente di eliminare i criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="46c0c-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="46c0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46c0c-107">EXAMPLES</span></span>

### <span data-ttu-id="46c0c-108">Esempio 1: abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="46c0c-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="46c0c-109">Questo comando consente di eliminare i criteri di conservazione per il servizio BLOB e di impostare i giorni di conservazione BLOB eliminati su 3.</span><span class="sxs-lookup"><span data-stu-id="46c0c-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="46c0c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46c0c-110">PARAMETERS</span></span>

### <span data-ttu-id="46c0c-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="46c0c-111">-Context</span></span>
<span data-ttu-id="46c0c-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="46c0c-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="46c0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c0c-113">-DefaultProfile</span></span>
<span data-ttu-id="46c0c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46c0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46c0c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46c0c-115">-PassThru</span></span>
<span data-ttu-id="46c0c-116">Visualizza DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="46c0c-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="46c0c-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="46c0c-117">-RetentionDays</span></span>
<span data-ttu-id="46c0c-118">Imposta il numero di giorni di conservazione per DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="46c0c-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="46c0c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="46c0c-119">-Confirm</span></span>
<span data-ttu-id="46c0c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46c0c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c0c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c0c-121">-WhatIf</span></span>
<span data-ttu-id="46c0c-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46c0c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46c0c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46c0c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c0c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c0c-124">CommonParameters</span></span>
<span data-ttu-id="46c0c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c0c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c0c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46c0c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c0c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46c0c-127">INPUTS</span></span>

### <span data-ttu-id="46c0c-128">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="46c0c-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="46c0c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46c0c-129">OUTPUTS</span></span>

### <span data-ttu-id="46c0c-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46c0c-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="46c0c-131">Note</span><span class="sxs-lookup"><span data-stu-id="46c0c-131">NOTES</span></span>

## <span data-ttu-id="46c0c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46c0c-132">RELATED LINKS</span></span>