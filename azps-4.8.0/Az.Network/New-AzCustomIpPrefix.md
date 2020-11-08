---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190982"
---
# <span data-ttu-id="35b21-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35b21-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="35b21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35b21-102">SYNOPSIS</span></span>
<span data-ttu-id="35b21-103">Crea una risorsa CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35b21-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="35b21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35b21-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35b21-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35b21-105">DESCRIPTION</span></span>
<span data-ttu-id="35b21-106">Il cmdlet **New-AzCustomIpPrefix** crea una risorsa CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="35b21-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="35b21-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35b21-107">EXAMPLES</span></span>

### <span data-ttu-id="35b21-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35b21-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="35b21-109">Questo comando crea una nuova risorsa CustomIpPrefix con il nome $prefixName nel gruppo di risorse $rgName con un CIDR di 40.40.40.0/24 in westus</span><span class="sxs-lookup"><span data-stu-id="35b21-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="35b21-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35b21-110">PARAMETERS</span></span>

### <span data-ttu-id="35b21-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35b21-111">-AsJob</span></span>
<span data-ttu-id="35b21-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="35b21-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35b21-113">-CIDR</span><span class="sxs-lookup"><span data-stu-id="35b21-113">-Cidr</span></span>
<span data-ttu-id="35b21-114">La notazione CIDR CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="35b21-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b21-115">-DefaultProfile</span></span>
<span data-ttu-id="35b21-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35b21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b21-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="35b21-117">-Location</span></span>
<span data-ttu-id="35b21-118">La posizione di CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="35b21-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b21-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="35b21-119">-Name</span></span>
<span data-ttu-id="35b21-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35b21-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b21-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35b21-121">-ResourceGroupName</span></span>
<span data-ttu-id="35b21-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="35b21-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b21-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="35b21-123">-Tag</span></span>
<span data-ttu-id="35b21-124">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="35b21-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b21-125">-Zona</span><span class="sxs-lookup"><span data-stu-id="35b21-125">-Zone</span></span>
<span data-ttu-id="35b21-126">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="35b21-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b21-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35b21-127">-Confirm</span></span>
<span data-ttu-id="35b21-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35b21-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35b21-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35b21-129">-WhatIf</span></span>
<span data-ttu-id="35b21-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35b21-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35b21-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35b21-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35b21-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b21-132">CommonParameters</span></span>
<span data-ttu-id="35b21-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35b21-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b21-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35b21-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b21-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35b21-135">INPUTS</span></span>

### <span data-ttu-id="35b21-136">System. String</span><span class="sxs-lookup"><span data-stu-id="35b21-136">System.String</span></span>

### <span data-ttu-id="35b21-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="35b21-137">System.String[]</span></span>

### <span data-ttu-id="35b21-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="35b21-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="35b21-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35b21-139">OUTPUTS</span></span>

### <span data-ttu-id="35b21-140">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35b21-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="35b21-141">Note</span><span class="sxs-lookup"><span data-stu-id="35b21-141">NOTES</span></span>

## <span data-ttu-id="35b21-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35b21-142">RELATED LINKS</span></span>

[<span data-ttu-id="35b21-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35b21-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="35b21-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35b21-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="35b21-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="35b21-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)