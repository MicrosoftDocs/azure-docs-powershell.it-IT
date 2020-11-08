---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023639"
---
# <span data-ttu-id="8261c-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8261c-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="8261c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8261c-102">SYNOPSIS</span></span>
<span data-ttu-id="8261c-103">Esporta l'immagine del modello di una raccolta RemoteApp di Azure nell'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="8261c-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="8261c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8261c-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8261c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8261c-105">DESCRIPTION</span></span>
<span data-ttu-id="8261c-106">Il cmdlet **Export-AzureRemoteAppTemplateImage** Esporta l'immagine del modello di una raccolta RemoteApp di Azure nell'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="8261c-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="8261c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8261c-107">EXAMPLES</span></span>

### <span data-ttu-id="8261c-108">Esempio 1: esportare un'immagine modello nell'account di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="8261c-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="8261c-109">Questo comando Esporta l'immagine del modello della raccolta denominata Contoso in un contenitore denominato ContainerName nell'account di archiviazione di Azure specificato con nome AccountName e Key AccountKey.</span><span class="sxs-lookup"><span data-stu-id="8261c-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="8261c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8261c-110">PARAMETERS</span></span>

### <span data-ttu-id="8261c-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="8261c-111">-CollectionName</span></span>
<span data-ttu-id="8261c-112">Specifica il nome della raccolta RemoteApp di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="8261c-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8261c-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="8261c-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="8261c-114">Specifica il nome di un contenitore nell'account di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8261c-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8261c-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8261c-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="8261c-116">Specifica la chiave dell'account di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8261c-116">Specifies the key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8261c-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8261c-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="8261c-118">Specifica il nome dell'account di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8261c-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8261c-119">-OverwriteExistingTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8261c-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="8261c-120">Indica che il cmdlet sovrascrive l'immagine del modello esistente.</span><span class="sxs-lookup"><span data-stu-id="8261c-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8261c-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="8261c-121">-Profile</span></span>
<span data-ttu-id="8261c-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8261c-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8261c-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8261c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8261c-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8261c-124">-Confirm</span></span>
<span data-ttu-id="8261c-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8261c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8261c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8261c-126">-WhatIf</span></span>
<span data-ttu-id="8261c-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8261c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8261c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8261c-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8261c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8261c-129">CommonParameters</span></span>
<span data-ttu-id="8261c-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8261c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8261c-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8261c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8261c-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8261c-132">INPUTS</span></span>

## <span data-ttu-id="8261c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8261c-133">OUTPUTS</span></span>

## <span data-ttu-id="8261c-134">Note</span><span class="sxs-lookup"><span data-stu-id="8261c-134">NOTES</span></span>

## <span data-ttu-id="8261c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8261c-135">RELATED LINKS</span></span>

[<span data-ttu-id="8261c-136">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8261c-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="8261c-137">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8261c-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="8261c-138">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8261c-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="8261c-139">Rinominare-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8261c-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


