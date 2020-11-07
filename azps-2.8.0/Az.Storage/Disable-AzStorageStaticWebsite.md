---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 4d5a12136dc23375e7ac5ea822c663c018f3bf68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857202"
---
# <span data-ttu-id="4d7fe-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4d7fe-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="4d7fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7fe-103">Disabilitare il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d7fe-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="4d7fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d7fe-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d7fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d7fe-105">DESCRIPTION</span></span>
<span data-ttu-id="4d7fe-106">Il cmdlet **Disable-AzStorageStaticWebsite Disabilita** il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d7fe-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="4d7fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d7fe-107">EXAMPLES</span></span>

### <span data-ttu-id="4d7fe-108">Esempio 1: disabilitare il sito Web statico per un account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="4d7fe-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="4d7fe-109">Questo comando Disabilita il sito Web statico per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d7fe-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="4d7fe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d7fe-110">PARAMETERS</span></span>

### <span data-ttu-id="4d7fe-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4d7fe-111">-Context</span></span>
<span data-ttu-id="4d7fe-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="4d7fe-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="4d7fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7fe-113">-DefaultProfile</span></span>
<span data-ttu-id="4d7fe-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d7fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d7fe-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d7fe-115">-PassThru</span></span>
<span data-ttu-id="4d7fe-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4d7fe-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4d7fe-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d7fe-117">-Confirm</span></span>
<span data-ttu-id="4d7fe-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d7fe-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d7fe-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d7fe-119">-WhatIf</span></span>
<span data-ttu-id="4d7fe-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d7fe-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d7fe-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d7fe-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d7fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7fe-122">CommonParameters</span></span>
<span data-ttu-id="4d7fe-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d7fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7fe-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d7fe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7fe-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d7fe-125">INPUTS</span></span>

### <span data-ttu-id="4d7fe-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4d7fe-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4d7fe-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d7fe-127">OUTPUTS</span></span>

### <span data-ttu-id="4d7fe-128">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="4d7fe-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="4d7fe-129">Note</span><span class="sxs-lookup"><span data-stu-id="4d7fe-129">NOTES</span></span>

## <span data-ttu-id="4d7fe-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d7fe-130">RELATED LINKS</span></span>
