---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: cd9270d724e0e1523c3ee621cb58fa28a2f4bc66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364041"
---
# <span data-ttu-id="12725-101">Set-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="12725-101">Set-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="12725-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12725-102">SYNOPSIS</span></span>
<span data-ttu-id="12725-103">Gruppo di zone DNS aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="12725-103">Updates DNS zone group</span></span>

## <span data-ttu-id="12725-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12725-104">SYNTAX</span></span>

```
Set-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12725-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12725-105">DESCRIPTION</span></span>
<span data-ttu-id="12725-106">Il cmdlet **set-AzPrivateDnsZoneGroup** aggiorna il gruppo di zone DNS.</span><span class="sxs-lookup"><span data-stu-id="12725-106">The **Set-AzPrivateDnsZoneGroup** cmdlet updates DNS zone group.</span></span>

## <span data-ttu-id="12725-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12725-107">EXAMPLES</span></span>

### <span data-ttu-id="12725-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12725-108">Example 1</span></span>
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

<span data-ttu-id="12725-109">L'esempio precedente aggiorna il gruppo di zone DNS denominato dnsgroup1 con un nuovo dnsconfig che si collega a un'altra zona DNS.</span><span class="sxs-lookup"><span data-stu-id="12725-109">Above example updates DNS zone group named dnsgroup1 with a new dnsconfig which links to another DNS zone.</span></span>

## <span data-ttu-id="12725-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12725-110">PARAMETERS</span></span>

### <span data-ttu-id="12725-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12725-111">-AsJob</span></span>
<span data-ttu-id="12725-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="12725-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12725-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12725-113">-DefaultProfile</span></span>
<span data-ttu-id="12725-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12725-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12725-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="12725-115">-Name</span></span>
<span data-ttu-id="12725-116">Nome del gruppo di aree private DNS.</span><span class="sxs-lookup"><span data-stu-id="12725-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="12725-117">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="12725-117">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="12725-118">Una raccolta di configurazioni di aree DNS private del gruppo di aree private DNS.</span><span class="sxs-lookup"><span data-stu-id="12725-118">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="12725-119">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="12725-119">-PrivateEndpointName</span></span>
<span data-ttu-id="12725-120">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="12725-120">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="12725-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12725-121">-ResourceGroupName</span></span>
<span data-ttu-id="12725-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12725-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="12725-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12725-123">-Confirm</span></span>
<span data-ttu-id="12725-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12725-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12725-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12725-125">-WhatIf</span></span>
<span data-ttu-id="12725-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12725-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12725-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12725-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12725-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12725-128">CommonParameters</span></span>
<span data-ttu-id="12725-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12725-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12725-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12725-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12725-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12725-131">INPUTS</span></span>

### <span data-ttu-id="12725-132">System. String</span><span class="sxs-lookup"><span data-stu-id="12725-132">System.String</span></span>

### <span data-ttu-id="12725-133">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="12725-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="12725-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12725-134">OUTPUTS</span></span>

### <span data-ttu-id="12725-135">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="12725-135">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="12725-136">Note</span><span class="sxs-lookup"><span data-stu-id="12725-136">NOTES</span></span>

## <span data-ttu-id="12725-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12725-137">RELATED LINKS</span></span>
