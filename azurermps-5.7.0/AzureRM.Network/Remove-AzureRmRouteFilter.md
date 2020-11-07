---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
ms.openlocfilehash: 5fcdbeee663873292b463bf774762c9de5418b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687640"
---
# <span data-ttu-id="43139-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="43139-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="43139-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43139-102">SYNOPSIS</span></span>
<span data-ttu-id="43139-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="43139-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43139-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43139-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43139-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43139-105">DESCRIPTION</span></span>
<span data-ttu-id="43139-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="43139-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="43139-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43139-107">EXAMPLES</span></span>

### <span data-ttu-id="43139-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43139-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="43139-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="43139-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="43139-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43139-110">PARAMETERS</span></span>

### <span data-ttu-id="43139-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43139-111">-DefaultProfile</span></span>
<span data-ttu-id="43139-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43139-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43139-113">-Force</span><span class="sxs-lookup"><span data-stu-id="43139-113">-Force</span></span>
<span data-ttu-id="43139-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="43139-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="43139-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="43139-115">-Name</span></span>
<span data-ttu-id="43139-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="43139-116">The resource name.</span></span>

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

### <span data-ttu-id="43139-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43139-117">-PassThru</span></span>
<span data-ttu-id="43139-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="43139-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="43139-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43139-119">-ResourceGroupName</span></span>
<span data-ttu-id="43139-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43139-120">The resource group name.</span></span>

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

### <span data-ttu-id="43139-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43139-121">-Confirm</span></span>
<span data-ttu-id="43139-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43139-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43139-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43139-123">-WhatIf</span></span>
<span data-ttu-id="43139-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43139-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43139-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43139-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43139-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43139-126">CommonParameters</span></span>
<span data-ttu-id="43139-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43139-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43139-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43139-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43139-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43139-129">INPUTS</span></span>

### <span data-ttu-id="43139-130">System. String</span><span class="sxs-lookup"><span data-stu-id="43139-130">System.String</span></span>

## <span data-ttu-id="43139-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43139-131">OUTPUTS</span></span>

### <span data-ttu-id="43139-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="43139-132">System.Object</span></span>

## <span data-ttu-id="43139-133">Note</span><span class="sxs-lookup"><span data-stu-id="43139-133">NOTES</span></span>

## <span data-ttu-id="43139-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43139-134">RELATED LINKS</span></span>

