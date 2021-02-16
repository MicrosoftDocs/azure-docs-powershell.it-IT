---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187846"
---
# <span data-ttu-id="f2b6b-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f2b6b-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="f2b6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b6b-103">Disabilitare il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b6b-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="f2b6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2b6b-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b6b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b6b-106">Il cmdlet **Disable-AzStorageStaticWebsite** disabilita il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b6b-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="f2b6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2b6b-107">EXAMPLES</span></span>

### <span data-ttu-id="f2b6b-108">Esempio 1: Disabilitare il sito Web statico per un account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="f2b6b-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="f2b6b-109">Questo comando disabilita il sito Web statico per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b6b-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="f2b6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2b6b-110">PARAMETERS</span></span>

### <span data-ttu-id="f2b6b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f2b6b-111">-Context</span></span>
<span data-ttu-id="f2b6b-112">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="f2b6b-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f2b6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b6b-113">-DefaultProfile</span></span>
<span data-ttu-id="f2b6b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2b6b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2b6b-115">-PassThru</span></span>
<span data-ttu-id="f2b6b-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f2b6b-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f2b6b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2b6b-117">-Confirm</span></span>
<span data-ttu-id="f2b6b-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2b6b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b6b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b6b-119">-WhatIf</span></span>
<span data-ttu-id="f2b6b-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2b6b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b6b-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2b6b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b6b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b6b-122">CommonParameters</span></span>
<span data-ttu-id="f2b6b-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b6b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b6b-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b6b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b6b-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2b6b-125">INPUTS</span></span>

### <span data-ttu-id="f2b6b-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f2b6b-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f2b6b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2b6b-127">OUTPUTS</span></span>

### <span data-ttu-id="f2b6b-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="f2b6b-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="f2b6b-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2b6b-129">NOTES</span></span>

## <span data-ttu-id="f2b6b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2b6b-130">RELATED LINKS</span></span>
