---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ec1f3e70752a5386cd5dad78d867da68091b96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491485"
---
# <span data-ttu-id="69499-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="69499-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="69499-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69499-102">SYNOPSIS</span></span>
<span data-ttu-id="69499-103">Aggiungere un'immagine della piattaforma macchina virtuale da una configurazione di immagine specificata.</span><span class="sxs-lookup"><span data-stu-id="69499-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="69499-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69499-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69499-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69499-105">DESCRIPTION</span></span>
<span data-ttu-id="69499-106">Aggiungere un'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="69499-106">Add a platform image.</span></span>

## <span data-ttu-id="69499-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69499-107">EXAMPLES</span></span>

### <span data-ttu-id="69499-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="69499-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="69499-109">Aggiungere una nuova immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="69499-109">Add a new platform image.</span></span>

## <span data-ttu-id="69499-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69499-110">PARAMETERS</span></span>

### <span data-ttu-id="69499-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69499-111">-AsJob</span></span>
<span data-ttu-id="69499-112">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="69499-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="69499-113">-BillingPartNumber</span></span>
<span data-ttu-id="69499-114">Il numero di parte viene usato per fatturare i costi del software.</span><span class="sxs-lookup"><span data-stu-id="69499-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-115">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="69499-115">-DataDisks</span></span>
<span data-ttu-id="69499-116">Dischi di dati usati dall'immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="69499-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-117">-Force</span><span class="sxs-lookup"><span data-stu-id="69499-117">-Force</span></span>
<span data-ttu-id="69499-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="69499-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="69499-119">-Location</span></span>
<span data-ttu-id="69499-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="69499-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-121">-Offerta</span><span class="sxs-lookup"><span data-stu-id="69499-121">-Offer</span></span>
<span data-ttu-id="69499-122">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="69499-122">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="69499-123">-OsType</span></span>
<span data-ttu-id="69499-124">Tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="69499-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="69499-125">-OsUri</span></span>
<span data-ttu-id="69499-126">Posizione del disco.</span><span class="sxs-lookup"><span data-stu-id="69499-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="69499-127">-Publisher</span></span>
<span data-ttu-id="69499-128">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="69499-128">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="69499-129">-Sku</span></span>
<span data-ttu-id="69499-130">Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="69499-130">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-131">-Versione</span><span class="sxs-lookup"><span data-stu-id="69499-131">-Version</span></span>
<span data-ttu-id="69499-132">Versione dell'immagine della piattaforma della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="69499-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69499-133">-Confirm</span></span>
<span data-ttu-id="69499-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69499-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69499-135">-WhatIf</span></span>
<span data-ttu-id="69499-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69499-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69499-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69499-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69499-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69499-138">CommonParameters</span></span>
<span data-ttu-id="69499-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69499-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69499-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69499-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69499-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69499-141">INPUTS</span></span>

## <span data-ttu-id="69499-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69499-142">OUTPUTS</span></span>

### <span data-ttu-id="69499-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="69499-143">PlatformImageObject</span></span>

## <span data-ttu-id="69499-144">Note</span><span class="sxs-lookup"><span data-stu-id="69499-144">NOTES</span></span>

## <span data-ttu-id="69499-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69499-145">RELATED LINKS</span></span>
