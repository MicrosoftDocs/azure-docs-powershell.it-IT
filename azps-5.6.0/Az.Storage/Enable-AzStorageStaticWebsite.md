---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: 25526e7c83746b67a5272ab94f3d523947795c1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973310"
---
# <span data-ttu-id="68a4b-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="68a4b-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="68a4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="68a4b-103">Abilitare il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="68a4b-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="68a4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68a4b-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68a4b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="68a4b-105">DESCRIPTION</span></span>
<span data-ttu-id="68a4b-106">Il cmdlet **Enable-AzStorageStaticWebsite** abilita il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="68a4b-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="68a4b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68a4b-107">EXAMPLES</span></span>

### <span data-ttu-id="68a4b-108">Esempio 1: Abilitare il sito Web statico per l'account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="68a4b-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="68a4b-109">Questo comando abilita il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="68a4b-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="68a4b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68a4b-110">PARAMETERS</span></span>

### <span data-ttu-id="68a4b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="68a4b-111">-Context</span></span>
<span data-ttu-id="68a4b-112">Oggetto contesto archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="68a4b-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="68a4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a4b-113">-DefaultProfile</span></span>
<span data-ttu-id="68a4b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68a4b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68a4b-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="68a4b-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="68a4b-116">Percorso del documento di errore che deve essere visualizzato quando viene generato il codice 404 (ovvero quando un browser richiede una pagina inesistente).</span><span class="sxs-lookup"><span data-stu-id="68a4b-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a4b-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="68a4b-117">-IndexDocument</span></span>
<span data-ttu-id="68a4b-118">Nome del documento di indice in ogni directory.</span><span class="sxs-lookup"><span data-stu-id="68a4b-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68a4b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68a4b-119">-PassThru</span></span>
<span data-ttu-id="68a4b-120">Visualizzare l'impostazione del sito Web statico in ServiceProperties.</span><span class="sxs-lookup"><span data-stu-id="68a4b-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="68a4b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68a4b-121">-Confirm</span></span>
<span data-ttu-id="68a4b-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68a4b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a4b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a4b-123">-WhatIf</span></span>
<span data-ttu-id="68a4b-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68a4b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68a4b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68a4b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a4b-126">CommonParameters</span></span>
<span data-ttu-id="68a4b-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a4b-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68a4b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a4b-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="68a4b-129">INPUTS</span></span>

### <span data-ttu-id="68a4b-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="68a4b-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="68a4b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68a4b-131">OUTPUTS</span></span>

### <span data-ttu-id="68a4b-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="68a4b-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="68a4b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="68a4b-133">NOTES</span></span>

## <span data-ttu-id="68a4b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68a4b-134">RELATED LINKS</span></span>
