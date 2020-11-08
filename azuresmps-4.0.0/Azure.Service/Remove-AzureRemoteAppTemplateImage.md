---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029611"
---
# <span data-ttu-id="8f11a-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8f11a-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="8f11a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f11a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f11a-103">Elimina un'immagine del modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f11a-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="8f11a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f11a-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f11a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f11a-105">DESCRIPTION</span></span>
<span data-ttu-id="8f11a-106">Il cmdlet **Remove-AzureRemoteAppTemplateImage** Elimina un'immagine del modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f11a-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="8f11a-107">Un'immagine del modello può essere eliminata solo se non è collegata a una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f11a-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8f11a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f11a-108">EXAMPLES</span></span>

### <span data-ttu-id="8f11a-109">Esempio 1: eliminare un'immagine del modello</span><span class="sxs-lookup"><span data-stu-id="8f11a-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="8f11a-110">Questo comando Elimina l'immagine del modello denominata ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="8f11a-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="8f11a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f11a-111">PARAMETERS</span></span>

### <span data-ttu-id="8f11a-112">-ImageName</span><span class="sxs-lookup"><span data-stu-id="8f11a-112">-ImageName</span></span>
<span data-ttu-id="8f11a-113">Specifica il nome dell'immagine del modello RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f11a-113">Specifies the name of the RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f11a-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="8f11a-114">-Profile</span></span>
<span data-ttu-id="8f11a-115">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f11a-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8f11a-116">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8f11a-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8f11a-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f11a-117">-Confirm</span></span>
<span data-ttu-id="8f11a-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f11a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f11a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f11a-119">-WhatIf</span></span>
<span data-ttu-id="8f11a-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f11a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f11a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f11a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f11a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f11a-122">CommonParameters</span></span>
<span data-ttu-id="8f11a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f11a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f11a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f11a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f11a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f11a-125">INPUTS</span></span>

## <span data-ttu-id="8f11a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f11a-126">OUTPUTS</span></span>

## <span data-ttu-id="8f11a-127">Note</span><span class="sxs-lookup"><span data-stu-id="8f11a-127">NOTES</span></span>

## <span data-ttu-id="8f11a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f11a-128">RELATED LINKS</span></span>

[<span data-ttu-id="8f11a-129">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8f11a-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="8f11a-130">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8f11a-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="8f11a-131">Rinominare-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8f11a-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


