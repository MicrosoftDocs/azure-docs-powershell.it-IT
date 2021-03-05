---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 0ac12ba420231d34c5ad278a8fd2a091fe4982da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960398"
---
# <span data-ttu-id="0272c-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0272c-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="0272c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0272c-102">SYNOPSIS</span></span>
<span data-ttu-id="0272c-103">Crea una risorsa CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0272c-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="0272c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0272c-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0272c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0272c-105">DESCRIPTION</span></span>
<span data-ttu-id="0272c-106">Il cmdlet **New-AzCustomIpPrefix** crea una risorsa CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="0272c-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="0272c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0272c-107">EXAMPLES</span></span>

### <span data-ttu-id="0272c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0272c-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="0272c-109">Questo comando crea una nuova risorsa CustomIpPrefix con il nome $prefixName nel gruppo di risorse $rgName con un cidr di 40.40.40.0/24 in ovest</span><span class="sxs-lookup"><span data-stu-id="0272c-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="0272c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0272c-110">PARAMETERS</span></span>

### <span data-ttu-id="0272c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0272c-111">-AsJob</span></span>
<span data-ttu-id="0272c-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0272c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0272c-113">-Cidr</span><span class="sxs-lookup"><span data-stu-id="0272c-113">-Cidr</span></span>
<span data-ttu-id="0272c-114">Lo strumento CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="0272c-114">The CustomIpPrefix CIDR.</span></span>

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

### <span data-ttu-id="0272c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0272c-115">-DefaultProfile</span></span>
<span data-ttu-id="0272c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0272c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0272c-117">-Location</span><span class="sxs-lookup"><span data-stu-id="0272c-117">-Location</span></span>
<span data-ttu-id="0272c-118">Posizione di CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="0272c-118">The CustomIpPrefix location.</span></span>

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

### <span data-ttu-id="0272c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0272c-119">-Name</span></span>
<span data-ttu-id="0272c-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0272c-120">The resource name.</span></span>

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

### <span data-ttu-id="0272c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0272c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0272c-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0272c-122">The resource group name.</span></span>

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

### <span data-ttu-id="0272c-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="0272c-123">-Tag</span></span>
<span data-ttu-id="0272c-124">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0272c-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0272c-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="0272c-125">-Zone</span></span>
<span data-ttu-id="0272c-126">Elenco di aree di disponibilità che denota l'indirizzo IP allocato per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0272c-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="0272c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0272c-127">-Confirm</span></span>
<span data-ttu-id="0272c-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0272c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0272c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0272c-129">-WhatIf</span></span>
<span data-ttu-id="0272c-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0272c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0272c-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0272c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0272c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0272c-132">CommonParameters</span></span>
<span data-ttu-id="0272c-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0272c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0272c-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0272c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0272c-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="0272c-135">INPUTS</span></span>

### <span data-ttu-id="0272c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0272c-136">System.String</span></span>

### <span data-ttu-id="0272c-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0272c-137">System.String[]</span></span>

### <span data-ttu-id="0272c-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0272c-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0272c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0272c-139">OUTPUTS</span></span>

### <span data-ttu-id="0272c-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0272c-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="0272c-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="0272c-141">NOTES</span></span>

## <span data-ttu-id="0272c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0272c-142">RELATED LINKS</span></span>

[<span data-ttu-id="0272c-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0272c-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="0272c-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0272c-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="0272c-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0272c-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)