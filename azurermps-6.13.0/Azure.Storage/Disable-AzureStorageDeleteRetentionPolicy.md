---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 656fe09054b1cfae90175cc4ea55370f80dfd8e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509495"
---
# <span data-ttu-id="bf8d6-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf8d6-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bf8d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf8d6-103">Disabilitare i criteri di conservazione Elimina per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf8d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf8d6-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf8d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="bf8d6-106">Il cmdlet **Disable-AzureStorageDeleteRetentionPolicy Disabilita** l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bf8d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf8d6-107">EXAMPLES</span></span>

### <span data-ttu-id="bf8d6-108">Esempio 1: disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="bf8d6-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="bf8d6-109">Questo comando Disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="bf8d6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf8d6-110">PARAMETERS</span></span>

### <span data-ttu-id="bf8d6-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bf8d6-111">-Context</span></span>
<span data-ttu-id="bf8d6-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="bf8d6-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="bf8d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf8d6-113">-DefaultProfile</span></span>
<span data-ttu-id="bf8d6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf8d6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf8d6-115">-PassThru</span></span>
<span data-ttu-id="bf8d6-116">Visualizza DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="bf8d6-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="bf8d6-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bf8d6-117">-Confirm</span></span>
<span data-ttu-id="bf8d6-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf8d6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf8d6-119">-WhatIf</span></span>
<span data-ttu-id="bf8d6-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf8d6-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf8d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf8d6-122">CommonParameters</span></span>
<span data-ttu-id="bf8d6-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf8d6-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf8d6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf8d6-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf8d6-125">INPUTS</span></span>

### <span data-ttu-id="bf8d6-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf8d6-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bf8d6-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf8d6-127">OUTPUTS</span></span>

### <span data-ttu-id="bf8d6-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bf8d6-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bf8d6-129">Note</span><span class="sxs-lookup"><span data-stu-id="bf8d6-129">NOTES</span></span>

## <span data-ttu-id="bf8d6-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf8d6-130">RELATED LINKS</span></span>
