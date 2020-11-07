---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
ms.openlocfilehash: d899b34e2f880a0351ce4d10f360f7bc29011b0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866413"
---
# <span data-ttu-id="fb958-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fb958-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="fb958-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb958-102">SYNOPSIS</span></span>
<span data-ttu-id="fb958-103">Disabilitare i criteri di conservazione Elimina per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fb958-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb958-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb958-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb958-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb958-105">DESCRIPTION</span></span>
<span data-ttu-id="fb958-106">Il cmdlet **Disable-AzureStorageDeleteRetentionPolicy Disabilita** l'eliminazione dei criteri di conservazione per il servizio BLOB di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fb958-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="fb958-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb958-107">EXAMPLES</span></span>

### <span data-ttu-id="fb958-108">Esempio 1: disabilitare l'eliminazione dei criteri di conservazione per il servizio BLOB</span><span class="sxs-lookup"><span data-stu-id="fb958-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="fb958-109">Questo comando Disabilita l'eliminazione dei criteri di conservazione per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="fb958-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="fb958-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb958-110">PARAMETERS</span></span>

### <span data-ttu-id="fb958-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fb958-111">-Context</span></span>
<span data-ttu-id="fb958-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="fb958-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="fb958-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb958-113">-DefaultProfile</span></span>
<span data-ttu-id="fb958-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb958-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb958-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb958-115">-PassThru</span></span>
<span data-ttu-id="fb958-116">Visualizza DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="fb958-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="fb958-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb958-117">-Confirm</span></span>
<span data-ttu-id="fb958-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb958-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb958-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb958-119">-WhatIf</span></span>
<span data-ttu-id="fb958-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb958-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb958-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb958-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb958-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb958-122">CommonParameters</span></span>
<span data-ttu-id="fb958-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb958-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb958-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb958-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb958-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb958-125">INPUTS</span></span>

### <span data-ttu-id="fb958-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fb958-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fb958-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb958-127">OUTPUTS</span></span>

### <span data-ttu-id="fb958-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fb958-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="fb958-129">Note</span><span class="sxs-lookup"><span data-stu-id="fb958-129">NOTES</span></span>

## <span data-ttu-id="fb958-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb958-130">RELATED LINKS</span></span>
