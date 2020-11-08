---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199481"
---
# <span data-ttu-id="e794d-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e794d-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="e794d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e794d-102">SYNOPSIS</span></span>
<span data-ttu-id="e794d-103">Abilitare il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e794d-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="e794d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e794d-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e794d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e794d-105">DESCRIPTION</span></span>
<span data-ttu-id="e794d-106">Il cmdlet **Enable-AzStorageStaticWebsite** Abilita il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e794d-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="e794d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e794d-107">EXAMPLES</span></span>

### <span data-ttu-id="e794d-108">Esempio 1: abilitare il sito Web statico per l'account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="e794d-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="e794d-109">Questo comando consente di abilitare il sito Web statico per l'account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e794d-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="e794d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e794d-110">PARAMETERS</span></span>

### <span data-ttu-id="e794d-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e794d-111">-Context</span></span>
<span data-ttu-id="e794d-112">Oggetto contesto di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="e794d-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e794d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e794d-113">-DefaultProfile</span></span>
<span data-ttu-id="e794d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e794d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e794d-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="e794d-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="e794d-116">Percorso del documento di errore che deve essere visualizzato quando viene emesso un 404, ovvero quando un browser richiede una pagina che non esiste.</span><span class="sxs-lookup"><span data-stu-id="e794d-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

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

### <span data-ttu-id="e794d-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="e794d-117">-IndexDocument</span></span>
<span data-ttu-id="e794d-118">Nome del documento di indice in ogni directory.</span><span class="sxs-lookup"><span data-stu-id="e794d-118">The name of the index document in each directory.</span></span>

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

### <span data-ttu-id="e794d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e794d-119">-PassThru</span></span>
<span data-ttu-id="e794d-120">Visualizzare l'impostazione statica del sito Web in ServiceProperties.</span><span class="sxs-lookup"><span data-stu-id="e794d-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="e794d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e794d-121">-Confirm</span></span>
<span data-ttu-id="e794d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e794d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e794d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e794d-123">-WhatIf</span></span>
<span data-ttu-id="e794d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e794d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e794d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e794d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e794d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e794d-126">CommonParameters</span></span>
<span data-ttu-id="e794d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e794d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e794d-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e794d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e794d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e794d-129">INPUTS</span></span>

### <span data-ttu-id="e794d-130">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e794d-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e794d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e794d-131">OUTPUTS</span></span>

### <span data-ttu-id="e794d-132">Microsoft. WindowsAzure. Commands. storage. Model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="e794d-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="e794d-133">Note</span><span class="sxs-lookup"><span data-stu-id="e794d-133">NOTES</span></span>

## <span data-ttu-id="e794d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e794d-134">RELATED LINKS</span></span>