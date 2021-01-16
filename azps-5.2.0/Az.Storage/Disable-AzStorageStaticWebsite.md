---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: a7814734f33e0a68fefacf4e465c1834cce17708
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349804"
---
# <span data-ttu-id="2df3f-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2df3f-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="2df3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2df3f-102">SYNOPSIS</span></span>
<span data-ttu-id="2df3f-103">Disabilitare il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2df3f-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="2df3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2df3f-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df3f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2df3f-105">DESCRIPTION</span></span>
<span data-ttu-id="2df3f-106">Il cmdlet **Disable-AzStorageStaticWebsite Disabilita** il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2df3f-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="2df3f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2df3f-107">EXAMPLES</span></span>

### <span data-ttu-id="2df3f-108">Esempio 1: disabilitare il sito Web statico per un account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="2df3f-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="2df3f-109">Questo comando Disabilita il sito Web statico per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2df3f-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="2df3f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2df3f-110">PARAMETERS</span></span>

### <span data-ttu-id="2df3f-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2df3f-111">-Context</span></span>
<span data-ttu-id="2df3f-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="2df3f-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2df3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df3f-113">-DefaultProfile</span></span>
<span data-ttu-id="2df3f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2df3f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2df3f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2df3f-115">-PassThru</span></span>
<span data-ttu-id="2df3f-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2df3f-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2df3f-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2df3f-117">-Confirm</span></span>
<span data-ttu-id="2df3f-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2df3f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df3f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df3f-119">-WhatIf</span></span>
<span data-ttu-id="2df3f-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2df3f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2df3f-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2df3f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df3f-122">CommonParameters</span></span>
<span data-ttu-id="2df3f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df3f-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df3f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df3f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2df3f-125">INPUTS</span></span>

### <span data-ttu-id="2df3f-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2df3f-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2df3f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2df3f-127">OUTPUTS</span></span>

### <span data-ttu-id="2df3f-128">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="2df3f-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="2df3f-129">Note</span><span class="sxs-lookup"><span data-stu-id="2df3f-129">NOTES</span></span>

## <span data-ttu-id="2df3f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2df3f-130">RELATED LINKS</span></span>
