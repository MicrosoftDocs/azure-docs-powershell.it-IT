---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b50cd7f98fd9919ed816314d7cec1222e5c4970c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490958"
---
# <span data-ttu-id="eb506-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="eb506-101">New-AzsIpPool</span></span>

## <span data-ttu-id="eb506-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb506-102">SYNOPSIS</span></span>
<span data-ttu-id="eb506-103">Creare un pool IP dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="eb506-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="eb506-104">Non è possibile eliminare o modificare una volta creato un pool IP.</span><span class="sxs-lookup"><span data-stu-id="eb506-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="eb506-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb506-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb506-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb506-106">DESCRIPTION</span></span>
<span data-ttu-id="eb506-107">Creare un pool IP dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="eb506-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="eb506-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb506-108">EXAMPLES</span></span>

### <span data-ttu-id="eb506-109">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb506-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="eb506-110">Creare un nuovo pool IP.</span><span class="sxs-lookup"><span data-stu-id="eb506-110">Create a new IP pool.</span></span>

## <span data-ttu-id="eb506-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb506-111">PARAMETERS</span></span>

### <span data-ttu-id="eb506-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="eb506-112">-AddressPrefix</span></span>
<span data-ttu-id="eb506-113">Prefisso dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="eb506-113">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb506-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb506-114">-AsJob</span></span>
<span data-ttu-id="eb506-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="eb506-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="eb506-116">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb506-116">-EndIpAddress</span></span>
<span data-ttu-id="eb506-117">Indirizzo IP finale.</span><span class="sxs-lookup"><span data-stu-id="eb506-117">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb506-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="eb506-118">-Location</span></span>
<span data-ttu-id="eb506-119">Area geografica in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb506-119">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb506-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb506-120">-Name</span></span>
<span data-ttu-id="eb506-121">Nome del pool IP.</span><span class="sxs-lookup"><span data-stu-id="eb506-121">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb506-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb506-122">-ResourceGroupName</span></span>
<span data-ttu-id="eb506-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb506-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb506-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb506-124">-StartIpAddress</span></span>
<span data-ttu-id="eb506-125">Indirizzo IP iniziale.</span><span class="sxs-lookup"><span data-stu-id="eb506-125">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb506-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb506-126">-Tags</span></span>
<span data-ttu-id="eb506-127">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="eb506-127">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb506-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eb506-128">-Confirm</span></span>
<span data-ttu-id="eb506-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb506-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb506-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb506-130">-WhatIf</span></span>
<span data-ttu-id="eb506-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb506-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb506-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb506-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb506-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb506-133">CommonParameters</span></span>
<span data-ttu-id="eb506-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb506-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb506-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb506-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb506-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb506-136">INPUTS</span></span>

## <span data-ttu-id="eb506-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb506-137">OUTPUTS</span></span>

### <span data-ttu-id="eb506-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="eb506-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="eb506-139">Note</span><span class="sxs-lookup"><span data-stu-id="eb506-139">NOTES</span></span>

## <span data-ttu-id="eb506-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb506-140">RELATED LINKS</span></span>
