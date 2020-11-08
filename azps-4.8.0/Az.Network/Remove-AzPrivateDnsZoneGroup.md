---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188400"
---
# <span data-ttu-id="3051d-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="3051d-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="3051d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3051d-102">SYNOPSIS</span></span>
<span data-ttu-id="3051d-103">Rimuove un gruppo di aree DNS.</span><span class="sxs-lookup"><span data-stu-id="3051d-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="3051d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3051d-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3051d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3051d-105">DESCRIPTION</span></span>
<span data-ttu-id="3051d-106">Il cmdlet **Remove-AzPrivateDnsZoneGroup** rimuove un gruppo di aree DNS.</span><span class="sxs-lookup"><span data-stu-id="3051d-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="3051d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3051d-107">EXAMPLES</span></span>

### <span data-ttu-id="3051d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3051d-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="3051d-109">Sopra l'esempio viene rimossa una zona DNS Grup denominata dnsgroup1 da endpoint test-PR-endpoint.</span><span class="sxs-lookup"><span data-stu-id="3051d-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="3051d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3051d-110">PARAMETERS</span></span>

### <span data-ttu-id="3051d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3051d-111">-AsJob</span></span>
<span data-ttu-id="3051d-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3051d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3051d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3051d-113">-DefaultProfile</span></span>
<span data-ttu-id="3051d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3051d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3051d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3051d-115">-Force</span></span>
<span data-ttu-id="3051d-116">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="3051d-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="3051d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3051d-117">-Name</span></span>
<span data-ttu-id="3051d-118">Nome del gruppo di aree private DNS.</span><span class="sxs-lookup"><span data-stu-id="3051d-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="3051d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3051d-119">-PassThru</span></span>
<span data-ttu-id="3051d-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3051d-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="3051d-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="3051d-121">-PrivateEndpointName</span></span>
<span data-ttu-id="3051d-122">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="3051d-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="3051d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3051d-123">-ResourceGroupName</span></span>
<span data-ttu-id="3051d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3051d-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="3051d-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3051d-125">-Confirm</span></span>
<span data-ttu-id="3051d-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3051d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3051d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3051d-127">-WhatIf</span></span>
<span data-ttu-id="3051d-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3051d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3051d-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3051d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3051d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3051d-130">CommonParameters</span></span>
<span data-ttu-id="3051d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3051d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3051d-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3051d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3051d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3051d-133">INPUTS</span></span>

### <span data-ttu-id="3051d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3051d-134">System.String</span></span>

## <span data-ttu-id="3051d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3051d-135">OUTPUTS</span></span>

### <span data-ttu-id="3051d-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3051d-136">System.Boolean</span></span>

## <span data-ttu-id="3051d-137">Note</span><span class="sxs-lookup"><span data-stu-id="3051d-137">NOTES</span></span>

## <span data-ttu-id="3051d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3051d-138">RELATED LINKS</span></span>
