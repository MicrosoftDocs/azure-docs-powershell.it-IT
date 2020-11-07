---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/add-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: d9ba42966efd4445fa561dff78b69d7e789badb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863985"
---
# <span data-ttu-id="bf108-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="bf108-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="bf108-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf108-102">SYNOPSIS</span></span>
<span data-ttu-id="bf108-103">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bf108-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="bf108-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf108-104">SYNTAX</span></span>

### <span data-ttu-id="bf108-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf108-105">CreateExpanded (Default)</span></span>
```
Add-AzsGalleryItem [-SubscriptionId <String>] [-GalleryItemUri <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bf108-106">Creare</span><span class="sxs-lookup"><span data-stu-id="bf108-106">Create</span></span>
```
Add-AzsGalleryItem -GalleryItemUriPayload <IGalleryItemUriPayload> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bf108-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf108-107">DESCRIPTION</span></span>
<span data-ttu-id="bf108-108">Carica un elemento della raccolta di provider nello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bf108-108">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="bf108-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf108-109">EXAMPLES</span></span>

### <span data-ttu-id="bf108-110">Esempio 1: Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="bf108-110">Example 1: Add-AzsGalleryItem</span></span>
```powershell
PS C:\> Add-AzsGalleryItem -GalleryItemUri https://testsa.blob.redmond.ext-n35r1010.masd.stbtest.microsoft.com/testsc/TestUbuntu.Test.1.0.0.azpkg

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM

```

<span data-ttu-id="bf108-111">Carica TestUbuntu. test. 1.0.0 nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="bf108-111">Uploads TestUbuntu.Test.1.0.0 to the gallery.</span></span>

## <span data-ttu-id="bf108-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf108-112">PARAMETERS</span></span>

### <span data-ttu-id="bf108-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf108-113">-DefaultProfile</span></span>
<span data-ttu-id="bf108-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf108-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bf108-115">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="bf108-115">-GalleryItemUri</span></span>
<span data-ttu-id="bf108-116">URI per il pacchetto della raccolta già caricato online.</span><span class="sxs-lookup"><span data-stu-id="bf108-116">URI for your gallery package that has already been uploaded online.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bf108-117">-GalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="bf108-117">-GalleryItemUriPayload</span></span>
<span data-ttu-id="bf108-118">Posizione del payload dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bf108-118">Location of gallery item payload.</span></span>
<span data-ttu-id="bf108-119">Per costruire, vedere la sezione Note per le proprietà di GALLERYITEMURIPAYLOAD e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bf108-119">To construct, see NOTES section for GALLERYITEMURIPAYLOAD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="bf108-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf108-120">-SubscriptionId</span></span>
<span data-ttu-id="bf108-121">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bf108-121">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bf108-122">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="bf108-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="bf108-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bf108-123">-Confirm</span></span>
<span data-ttu-id="bf108-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf108-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf108-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf108-125">-WhatIf</span></span>
<span data-ttu-id="bf108-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf108-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf108-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf108-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf108-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf108-128">CommonParameters</span></span>
<span data-ttu-id="bf108-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf108-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf108-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf108-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf108-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf108-131">INPUTS</span></span>

### <span data-ttu-id="bf108-132">Microsoft. Azure. PowerShell. Cmdlets. gallery. Models. Api20150401. IGalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="bf108-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload</span></span>

## <span data-ttu-id="bf108-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf108-133">OUTPUTS</span></span>

### <span data-ttu-id="bf108-134">Microsoft. Azure. PowerShell. Cmdlets. gallery. Models. Api20150401. IGalleryItem</span><span class="sxs-lookup"><span data-stu-id="bf108-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="bf108-135">Note</span><span class="sxs-lookup"><span data-stu-id="bf108-135">NOTES</span></span>

<span data-ttu-id="bf108-136">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bf108-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf108-137">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf108-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bf108-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload> : posizione del payload dell'elemento della raccolta.</span><span class="sxs-lookup"><span data-stu-id="bf108-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload>: Location of gallery item payload.</span></span>
  - <span data-ttu-id="bf108-139">`[GalleryItemUri <String>]`: URI per il pacchetto della raccolta già caricato online.</span><span class="sxs-lookup"><span data-stu-id="bf108-139">`[GalleryItemUri <String>]`: URI for your gallery package that has already been uploaded online.</span></span>

## <span data-ttu-id="bf108-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf108-140">RELATED LINKS</span></span>

