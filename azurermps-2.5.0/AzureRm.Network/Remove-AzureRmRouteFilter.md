---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 3622b7ad87658091d4b54af62678d12a324ef56a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866994"
---
# <span data-ttu-id="6d9d5-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6d9d5-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="6d9d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9d5-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="6d9d5-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d9d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d9d5-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d9d5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d9d5-105">DESCRIPTION</span></span>
<span data-ttu-id="6d9d5-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="6d9d5-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="6d9d5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d9d5-107">EXAMPLES</span></span>

### <span data-ttu-id="6d9d5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d9d5-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6d9d5-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="6d9d5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="6d9d5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d9d5-110">PARAMETERS</span></span>

### <span data-ttu-id="6d9d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9d5-111">-DefaultProfile</span></span>
<span data-ttu-id="6d9d5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9d5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6d9d5-113">-Force</span></span>
<span data-ttu-id="6d9d5-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6d9d5-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6d9d5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d9d5-115">-Name</span></span>
<span data-ttu-id="6d9d5-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d9d5-116">The resource name.</span></span>

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

### <span data-ttu-id="6d9d5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d9d5-117">-PassThru</span></span>
<span data-ttu-id="6d9d5-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6d9d5-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6d9d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d9d5-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d9d5-120">The resource group name.</span></span>

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

### <span data-ttu-id="6d9d5-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d9d5-121">-Confirm</span></span>
<span data-ttu-id="6d9d5-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d9d5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d9d5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d9d5-123">-WhatIf</span></span>
<span data-ttu-id="6d9d5-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d9d5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d9d5-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d9d5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d9d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9d5-126">CommonParameters</span></span>
<span data-ttu-id="6d9d5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9d5-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d9d5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9d5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d9d5-129">INPUTS</span></span>

### <span data-ttu-id="6d9d5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6d9d5-130">System.String</span></span>

## <span data-ttu-id="6d9d5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d9d5-131">OUTPUTS</span></span>

### <span data-ttu-id="6d9d5-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="6d9d5-132">System.Object</span></span>

## <span data-ttu-id="6d9d5-133">Note</span><span class="sxs-lookup"><span data-stu-id="6d9d5-133">NOTES</span></span>

## <span data-ttu-id="6d9d5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d9d5-134">RELATED LINKS</span></span>

