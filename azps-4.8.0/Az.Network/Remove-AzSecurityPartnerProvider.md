---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192039"
---
# <span data-ttu-id="e857e-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e857e-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="e857e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e857e-102">SYNOPSIS</span></span>
<span data-ttu-id="e857e-103">Elimina un SecurityPartnerProvider di Azure.</span><span class="sxs-lookup"><span data-stu-id="e857e-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="e857e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e857e-104">SYNTAX</span></span>

### <span data-ttu-id="e857e-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e857e-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e857e-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e857e-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e857e-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e857e-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e857e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e857e-108">DESCRIPTION</span></span>
<span data-ttu-id="e857e-109">Il cmdlet **Remove-AzSecurityPartnerProvider** Elimina un SecurityPartnerProvider di Azure</span><span class="sxs-lookup"><span data-stu-id="e857e-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="e857e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e857e-110">EXAMPLES</span></span>

### <span data-ttu-id="e857e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e857e-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="e857e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e857e-112">PARAMETERS</span></span>

### <span data-ttu-id="e857e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e857e-113">-AsJob</span></span>
<span data-ttu-id="e857e-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e857e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e857e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e857e-115">-DefaultProfile</span></span>
<span data-ttu-id="e857e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e857e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e857e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e857e-117">-Force</span></span>
<span data-ttu-id="e857e-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e857e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e857e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e857e-119">-Name</span></span>
<span data-ttu-id="e857e-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e857e-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e857e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e857e-121">-PassThru</span></span>
<span data-ttu-id="e857e-122">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e857e-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="e857e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e857e-123">-ResourceGroupName</span></span>
<span data-ttu-id="e857e-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e857e-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e857e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e857e-125">-ResourceId</span></span>
<span data-ttu-id="e857e-126">ID risorsa securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="e857e-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e857e-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e857e-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="e857e-128">L'oggetto di input securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="e857e-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e857e-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e857e-129">-Confirm</span></span>
<span data-ttu-id="e857e-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e857e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e857e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e857e-131">-WhatIf</span></span>
<span data-ttu-id="e857e-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e857e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e857e-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e857e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e857e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e857e-134">CommonParameters</span></span>
<span data-ttu-id="e857e-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e857e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e857e-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e857e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e857e-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e857e-137">INPUTS</span></span>

### <span data-ttu-id="e857e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e857e-138">System.String</span></span>

### <span data-ttu-id="e857e-139">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e857e-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="e857e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e857e-140">OUTPUTS</span></span>

### <span data-ttu-id="e857e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e857e-141">System.Boolean</span></span>

## <span data-ttu-id="e857e-142">Note</span><span class="sxs-lookup"><span data-stu-id="e857e-142">NOTES</span></span>

## <span data-ttu-id="e857e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e857e-143">RELATED LINKS</span></span>