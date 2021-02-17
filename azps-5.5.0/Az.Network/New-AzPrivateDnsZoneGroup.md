---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184406"
---
# <span data-ttu-id="5e48c-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="5e48c-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5e48c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e48c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e48c-103">Crea un gruppo di zona DNS privato nell'endpoint privato specificato.</span><span class="sxs-lookup"><span data-stu-id="5e48c-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="5e48c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e48c-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e48c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5e48c-105">DESCRIPTION</span></span>
<span data-ttu-id="5e48c-106">Il cmdlet **New-AzPrivateDnsZoneGroup** consente di creare un nuovo gruppo di zona DNS privato.</span><span class="sxs-lookup"><span data-stu-id="5e48c-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="5e48c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e48c-107">EXAMPLES</span></span>

### <span data-ttu-id="5e48c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e48c-108">Example 1</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
PS C:\> New-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1" -PrivateDnsZoneConfig $config -Force
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="5e48c-109">Dopo la creazione `test-pr-endpoint` dell'endpoint privato, nell'esempio precedente viene creato un gruppo di zona DNS in tale endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="5e48c-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="5e48c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e48c-110">PARAMETERS</span></span>

### <span data-ttu-id="5e48c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e48c-111">-AsJob</span></span>
<span data-ttu-id="5e48c-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5e48c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e48c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e48c-113">-DefaultProfile</span></span>
<span data-ttu-id="5e48c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e48c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e48c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5e48c-115">-Force</span></span>
<span data-ttu-id="5e48c-116">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="5e48c-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5e48c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5e48c-117">-Name</span></span>
<span data-ttu-id="5e48c-118">Nome del gruppo di zona DNS privato.</span><span class="sxs-lookup"><span data-stu-id="5e48c-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="5e48c-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="5e48c-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="5e48c-120">Raccolta di configurazioni di zona DNS private del gruppo di zona DNS privato.</span><span class="sxs-lookup"><span data-stu-id="5e48c-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e48c-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="5e48c-121">-PrivateEndpointName</span></span>
<span data-ttu-id="5e48c-122">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="5e48c-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="5e48c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e48c-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e48c-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e48c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e48c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e48c-125">-Confirm</span></span>
<span data-ttu-id="5e48c-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e48c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e48c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e48c-127">-WhatIf</span></span>
<span data-ttu-id="5e48c-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e48c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e48c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e48c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e48c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e48c-130">CommonParameters</span></span>
<span data-ttu-id="5e48c-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e48c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e48c-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e48c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e48c-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="5e48c-133">INPUTS</span></span>

### <span data-ttu-id="5e48c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5e48c-134">System.String</span></span>

### <span data-ttu-id="5e48c-135">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="5e48c-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5e48c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e48c-136">OUTPUTS</span></span>

### <span data-ttu-id="5e48c-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="5e48c-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5e48c-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="5e48c-138">NOTES</span></span>

## <span data-ttu-id="5e48c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e48c-139">RELATED LINKS</span></span>
