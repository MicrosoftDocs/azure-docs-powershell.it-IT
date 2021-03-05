---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: ada7faf13457f2c074a15b6e409e31afb93ac900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993549"
---
# <span data-ttu-id="39281-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="39281-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="39281-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39281-102">SYNOPSIS</span></span>
<span data-ttu-id="39281-103">Rimuove un gruppo di zona DNS.</span><span class="sxs-lookup"><span data-stu-id="39281-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="39281-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39281-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39281-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39281-105">DESCRIPTION</span></span>
<span data-ttu-id="39281-106">Il cmdlet **Remove-AzPrivateDnsZoneGroup** rimuove un gruppo di zona DNS.</span><span class="sxs-lookup"><span data-stu-id="39281-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="39281-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39281-107">EXAMPLES</span></span>

### <span data-ttu-id="39281-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39281-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="39281-109">L'esempio precedente rimuove un dns zone grup denominato dnsgroup1 dall'endpoint test-pr-endpoint.</span><span class="sxs-lookup"><span data-stu-id="39281-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="39281-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39281-110">PARAMETERS</span></span>

### <span data-ttu-id="39281-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39281-111">-AsJob</span></span>
<span data-ttu-id="39281-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="39281-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39281-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39281-113">-DefaultProfile</span></span>
<span data-ttu-id="39281-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39281-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39281-115">-Force</span><span class="sxs-lookup"><span data-stu-id="39281-115">-Force</span></span>
<span data-ttu-id="39281-116">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="39281-116">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39281-117">-Name</span><span class="sxs-lookup"><span data-stu-id="39281-117">-Name</span></span>
<span data-ttu-id="39281-118">Nome del gruppo di zona DNS privato.</span><span class="sxs-lookup"><span data-stu-id="39281-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39281-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39281-119">-PassThru</span></span>
<span data-ttu-id="39281-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="39281-120">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39281-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="39281-121">-PrivateEndpointName</span></span>
<span data-ttu-id="39281-122">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="39281-122">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39281-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39281-123">-ResourceGroupName</span></span>
<span data-ttu-id="39281-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39281-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39281-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39281-125">-Confirm</span></span>
<span data-ttu-id="39281-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39281-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39281-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39281-127">-WhatIf</span></span>
<span data-ttu-id="39281-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39281-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39281-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39281-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39281-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39281-130">CommonParameters</span></span>
<span data-ttu-id="39281-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39281-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39281-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39281-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39281-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="39281-133">INPUTS</span></span>

### <span data-ttu-id="39281-134">System.String</span><span class="sxs-lookup"><span data-stu-id="39281-134">System.String</span></span>

## <span data-ttu-id="39281-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39281-135">OUTPUTS</span></span>

### <span data-ttu-id="39281-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39281-136">System.Boolean</span></span>

## <span data-ttu-id="39281-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="39281-137">NOTES</span></span>

## <span data-ttu-id="39281-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39281-138">RELATED LINKS</span></span>
