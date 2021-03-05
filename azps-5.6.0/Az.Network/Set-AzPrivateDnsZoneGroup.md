---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 9ddd81b236303a15017bcd96da35774a16fae8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016174"
---
# <span data-ttu-id="ea7b1-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="ea7b1-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="ea7b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea7b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7b1-103">Aggiorna il gruppo di zona DNS</span><span class="sxs-lookup"><span data-stu-id="ea7b1-103">Updates DNS zone group</span></span>

## <span data-ttu-id="ea7b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea7b1-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7b1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea7b1-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7b1-106">Il cmdlet **Set-AzPrivateDnsZoneGroup** aggiorna il gruppo di zona DNS.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="ea7b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea7b1-107">EXAMPLES</span></span>

### <span data-ttu-id="ea7b1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea7b1-108">Example 1</span></span>
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

<span data-ttu-id="ea7b1-109">L'esempio precedente aggiorna il gruppo di zona DNS denominato dnsgroup1 con un nuovo dnsconfig, che si collega a un'altra zona DNS.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="ea7b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea7b1-110">PARAMETERS</span></span>

### <span data-ttu-id="ea7b1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea7b1-111">-AsJob</span></span>
<span data-ttu-id="ea7b1-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ea7b1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea7b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7b1-113">-DefaultProfile</span></span>
<span data-ttu-id="ea7b1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea7b1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ea7b1-115">-Name</span></span>
<span data-ttu-id="ea7b1-116">Nome del gruppo di zona DNS privato.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="ea7b1-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="ea7b1-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="ea7b1-118">Raccolta di configurazioni di zona DNS private del gruppo di zona DNS privato.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="ea7b1-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="ea7b1-119">-PrivateEndpointName</span></span>
<span data-ttu-id="ea7b1-120">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="ea7b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea7b1-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ea7b1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea7b1-123">-Confirm</span></span>
<span data-ttu-id="ea7b1-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7b1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7b1-125">-WhatIf</span></span>
<span data-ttu-id="ea7b1-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7b1-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7b1-128">CommonParameters</span></span>
<span data-ttu-id="ea7b1-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7b1-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea7b1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7b1-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea7b1-131">INPUTS</span></span>

### <span data-ttu-id="ea7b1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ea7b1-132">System.String</span></span>

### <span data-ttu-id="ea7b1-133">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="ea7b1-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ea7b1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea7b1-134">OUTPUTS</span></span>

### <span data-ttu-id="ea7b1-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="ea7b1-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="ea7b1-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea7b1-136">NOTES</span></span>

## <span data-ttu-id="ea7b1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea7b1-137">RELATED LINKS</span></span>
