---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 1d55c52b3c022e9e935051cdb1ad23aae32eecbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973357"
---
# <span data-ttu-id="bbd58-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd58-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bbd58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbd58-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd58-103">Abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd58-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bbd58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbd58-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbd58-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bbd58-105">DESCRIPTION</span></span>
<span data-ttu-id="bbd58-106">Il cmdlet **Enable-AzStorageDeleteRetentionPolicy** abilita l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd58-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bbd58-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbd58-107">EXAMPLES</span></span>

### <span data-ttu-id="bbd58-108">Esempio 1: Abilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="bbd58-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="bbd58-109">Questo comando abilita i criteri di conservazione per il servizio BLOB e imposta i giorni di conservazione BLOB eliminati su 3.</span><span class="sxs-lookup"><span data-stu-id="bbd58-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="bbd58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbd58-110">PARAMETERS</span></span>

### <span data-ttu-id="bbd58-111">-Context</span><span class="sxs-lookup"><span data-stu-id="bbd58-111">-Context</span></span>
<span data-ttu-id="bbd58-112">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="bbd58-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="bbd58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd58-113">-DefaultProfile</span></span>
<span data-ttu-id="bbd58-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd58-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbd58-115">-PassThru</span></span>
<span data-ttu-id="bbd58-116">Display DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="bbd58-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="bbd58-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="bbd58-117">-RetentionDays</span></span>
<span data-ttu-id="bbd58-118">Imposta il numero di giorni di conservazione per DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="bbd58-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="bbd58-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbd58-119">-Confirm</span></span>
<span data-ttu-id="bbd58-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd58-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd58-121">-WhatIf</span></span>
<span data-ttu-id="bbd58-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbd58-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd58-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbd58-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd58-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd58-124">CommonParameters</span></span>
<span data-ttu-id="bbd58-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd58-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd58-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd58-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd58-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="bbd58-127">INPUTS</span></span>

### <span data-ttu-id="bbd58-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbd58-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bbd58-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbd58-129">OUTPUTS</span></span>

### <span data-ttu-id="bbd58-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd58-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bbd58-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="bbd58-131">NOTES</span></span>

## <span data-ttu-id="bbd58-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbd58-132">RELATED LINKS</span></span>
