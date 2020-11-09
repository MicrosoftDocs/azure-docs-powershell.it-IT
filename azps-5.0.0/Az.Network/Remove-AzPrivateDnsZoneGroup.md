---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311394"
---
# <span data-ttu-id="d151f-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="d151f-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="d151f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d151f-102">SYNOPSIS</span></span>
<span data-ttu-id="d151f-103">Rimuove un gruppo di aree DNS.</span><span class="sxs-lookup"><span data-stu-id="d151f-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="d151f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d151f-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d151f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d151f-105">DESCRIPTION</span></span>
<span data-ttu-id="d151f-106">Il cmdlet **Remove-AzPrivateDnsZoneGroup** rimuove un gruppo di aree DNS.</span><span class="sxs-lookup"><span data-stu-id="d151f-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="d151f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d151f-107">EXAMPLES</span></span>

### <span data-ttu-id="d151f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d151f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="d151f-109">Sopra l'esempio viene rimossa una zona DNS Grup denominata dnsgroup1 da endpoint test-PR-endpoint.</span><span class="sxs-lookup"><span data-stu-id="d151f-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="d151f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d151f-110">PARAMETERS</span></span>

### <span data-ttu-id="d151f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d151f-111">-AsJob</span></span>
<span data-ttu-id="d151f-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d151f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d151f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d151f-113">-DefaultProfile</span></span>
<span data-ttu-id="d151f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d151f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d151f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d151f-115">-Force</span></span>
<span data-ttu-id="d151f-116">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="d151f-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="d151f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d151f-117">-Name</span></span>
<span data-ttu-id="d151f-118">Nome del gruppo di aree private DNS.</span><span class="sxs-lookup"><span data-stu-id="d151f-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="d151f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d151f-119">-PassThru</span></span>
<span data-ttu-id="d151f-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d151f-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d151f-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="d151f-121">-PrivateEndpointName</span></span>
<span data-ttu-id="d151f-122">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="d151f-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="d151f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d151f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d151f-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d151f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d151f-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d151f-125">-Confirm</span></span>
<span data-ttu-id="d151f-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d151f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d151f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d151f-127">-WhatIf</span></span>
<span data-ttu-id="d151f-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d151f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d151f-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d151f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d151f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d151f-130">CommonParameters</span></span>
<span data-ttu-id="d151f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d151f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d151f-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d151f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d151f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d151f-133">INPUTS</span></span>

### <span data-ttu-id="d151f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d151f-134">System.String</span></span>

## <span data-ttu-id="d151f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d151f-135">OUTPUTS</span></span>

### <span data-ttu-id="d151f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d151f-136">System.Boolean</span></span>

## <span data-ttu-id="d151f-137">Note</span><span class="sxs-lookup"><span data-stu-id="d151f-137">NOTES</span></span>

## <span data-ttu-id="d151f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d151f-138">RELATED LINKS</span></span>
