---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184182"
---
# <span data-ttu-id="1c8a6-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="1c8a6-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="1c8a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8a6-103">Aggiorna il gruppo di zona DNS</span><span class="sxs-lookup"><span data-stu-id="1c8a6-103">Updates DNS zone group</span></span>

## <span data-ttu-id="1c8a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c8a6-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c8a6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c8a6-105">DESCRIPTION</span></span>
<span data-ttu-id="1c8a6-106">Il cmdlet **Set-AzPrivateDnsZoneGroup** aggiorna il gruppo di zona DNS.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="1c8a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c8a6-107">EXAMPLES</span></span>

### <span data-ttu-id="1c8a6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c8a6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]

PS C:\> $zone1 = Get-AzPrivateDnsZone -ResourceGroupName rg -Name "test1.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name test1-vault-azure-com -PrivateDnsZoneId $zone1.ResourceId
PS C:\> Set-AzPrivateDnsZoneGroup -ResourceGroupName rg -PrivateEndpointName my-pr-endpoint -name dnsgroup1 -PrivateDnsZoneConfig $config -Force

Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/my-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test1-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test1.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="1c8a6-109">L'esempio precedente aggiorna il gruppo di zona DNS denominato dnsgroup1 con un nuovo dnsconfig, che si collega a un'altra zona DNS.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="1c8a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c8a6-110">PARAMETERS</span></span>

### <span data-ttu-id="1c8a6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c8a6-111">-AsJob</span></span>
<span data-ttu-id="1c8a6-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1c8a6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c8a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c8a6-113">-DefaultProfile</span></span>
<span data-ttu-id="1c8a6-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c8a6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1c8a6-115">-Name</span></span>
<span data-ttu-id="1c8a6-116">Nome del gruppo di zona DNS privato.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="1c8a6-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="1c8a6-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="1c8a6-118">Raccolta di configurazioni di zona DNS private del gruppo di zona DNS privato.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="1c8a6-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="1c8a6-119">-PrivateEndpointName</span></span>
<span data-ttu-id="1c8a6-120">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="1c8a6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c8a6-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c8a6-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="1c8a6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c8a6-123">-Confirm</span></span>
<span data-ttu-id="1c8a6-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c8a6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c8a6-125">-WhatIf</span></span>
<span data-ttu-id="1c8a6-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c8a6-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c8a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8a6-128">CommonParameters</span></span>
<span data-ttu-id="1c8a6-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8a6-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c8a6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8a6-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c8a6-131">INPUTS</span></span>

### <span data-ttu-id="1c8a6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1c8a6-132">System.String</span></span>

### <span data-ttu-id="1c8a6-133">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="1c8a6-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1c8a6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c8a6-134">OUTPUTS</span></span>

### <span data-ttu-id="1c8a6-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="1c8a6-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="1c8a6-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c8a6-136">NOTES</span></span>

## <span data-ttu-id="1c8a6-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c8a6-137">RELATED LINKS</span></span>
