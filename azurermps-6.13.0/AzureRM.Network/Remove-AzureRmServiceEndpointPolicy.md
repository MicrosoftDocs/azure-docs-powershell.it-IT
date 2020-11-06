---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520916"
---
# <span data-ttu-id="cfe26-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cfe26-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="cfe26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cfe26-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe26-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="cfe26-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfe26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfe26-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfe26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfe26-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe26-106">Il cmdlet **Remove-AzureRmServiceEndpointPolicy** rimuove un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="cfe26-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="cfe26-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfe26-107">EXAMPLES</span></span>

### <span data-ttu-id="cfe26-108">Esempio 1: rimuove un criterio endpoint di servizio tramite Name</span><span class="sxs-lookup"><span data-stu-id="cfe26-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="cfe26-109">Questo comando rimuove un criterio endpoint del servizio con il nome Policy1 che appartiene a ResourceGroup con nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="cfe26-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="cfe26-110">Esempio 2: rimuovere un criterio endpoint del servizio usando l'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="cfe26-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="cfe26-111">Questo comando rimuove un oggetto Criteri endpoint servizio Policy1 che appartiene a ResourceGroup con nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="cfe26-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="cfe26-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfe26-112">PARAMETERS</span></span>

### <span data-ttu-id="cfe26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe26-113">-DefaultProfile</span></span>
<span data-ttu-id="cfe26-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe26-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfe26-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cfe26-115">-Force</span></span>
<span data-ttu-id="cfe26-116">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="cfe26-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="cfe26-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfe26-117">-Name</span></span>
<span data-ttu-id="cfe26-118">Nome del criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="cfe26-118">The name of the service endpoint policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe26-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfe26-119">-PassThru</span></span>
<span data-ttu-id="cfe26-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cfe26-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cfe26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe26-121">-ResourceGroupName</span></span>
<span data-ttu-id="cfe26-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cfe26-122">The resource group name.</span></span>

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

### <span data-ttu-id="cfe26-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cfe26-123">-Confirm</span></span>
<span data-ttu-id="cfe26-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfe26-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe26-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe26-125">-WhatIf</span></span>
<span data-ttu-id="cfe26-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfe26-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfe26-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfe26-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfe26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe26-128">CommonParameters</span></span>
<span data-ttu-id="cfe26-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cfe26-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe26-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe26-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cfe26-131">INPUTS</span></span>

### <span data-ttu-id="cfe26-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe26-132">System.String</span></span>


## <span data-ttu-id="cfe26-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfe26-133">OUTPUTS</span></span>

### <span data-ttu-id="cfe26-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="cfe26-134">System.Object</span></span>

## <span data-ttu-id="cfe26-135">Note</span><span class="sxs-lookup"><span data-stu-id="cfe26-135">NOTES</span></span>

## <span data-ttu-id="cfe26-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfe26-136">RELATED LINKS</span></span>
