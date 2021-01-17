---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: fff326143cf2740a085a6fcc3daa5dc89cdee646
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330727"
---
# <span data-ttu-id="de5b8-101">New-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="de5b8-101">New-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="de5b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de5b8-102">SYNOPSIS</span></span>
<span data-ttu-id="de5b8-103">Crea un gruppo di aree DNS privato nell'endpoint privato specificato.</span><span class="sxs-lookup"><span data-stu-id="de5b8-103">Creates a private DNS zone group in the specified private endpoint.</span></span>

## <span data-ttu-id="de5b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de5b8-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 -PrivateDnsZoneConfig <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig]>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de5b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de5b8-105">DESCRIPTION</span></span>
<span data-ttu-id="de5b8-106">Il cmdlet **New-AzPrivateDnsZoneGroup** consente di creare un nuovo gruppo di aree DNS private.</span><span class="sxs-lookup"><span data-stu-id="de5b8-106">The **New-AzPrivateDnsZoneGroup** cmdlet enables you to create a new private DNS zone group.</span></span>

## <span data-ttu-id="de5b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de5b8-107">EXAMPLES</span></span>

### <span data-ttu-id="de5b8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de5b8-108">Example 1</span></span>
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

<span data-ttu-id="de5b8-109">Una volta creato endpoint privato `test-pr-endpoint` , sopra l'esempio viene creato il gruppo di zone DNS in tale endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="de5b8-109">Once private endpoint `test-pr-endpoint` is created, above example creates DNS zone group under that private endpoint.</span></span>

## <span data-ttu-id="de5b8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de5b8-110">PARAMETERS</span></span>

### <span data-ttu-id="de5b8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de5b8-111">-AsJob</span></span>
<span data-ttu-id="de5b8-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="de5b8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de5b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5b8-113">-DefaultProfile</span></span>
<span data-ttu-id="de5b8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de5b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de5b8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="de5b8-115">-Force</span></span>
<span data-ttu-id="de5b8-116">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="de5b8-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="de5b8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="de5b8-117">-Name</span></span>
<span data-ttu-id="de5b8-118">Nome del gruppo di aree private DNS.</span><span class="sxs-lookup"><span data-stu-id="de5b8-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="de5b8-119">-PrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="de5b8-119">-PrivateDnsZoneConfig</span></span>
<span data-ttu-id="de5b8-120">Una raccolta di configurazioni di aree DNS private del gruppo di aree private DNS.</span><span class="sxs-lookup"><span data-stu-id="de5b8-120">A collection of private dns zone configurations of the private dns zone group.</span></span>

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

### <span data-ttu-id="de5b8-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="de5b8-121">-PrivateEndpointName</span></span>
<span data-ttu-id="de5b8-122">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="de5b8-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="de5b8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de5b8-123">-ResourceGroupName</span></span>
<span data-ttu-id="de5b8-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de5b8-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="de5b8-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de5b8-125">-Confirm</span></span>
<span data-ttu-id="de5b8-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de5b8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de5b8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5b8-127">-WhatIf</span></span>
<span data-ttu-id="de5b8-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de5b8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de5b8-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de5b8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de5b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5b8-130">CommonParameters</span></span>
<span data-ttu-id="de5b8-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de5b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5b8-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de5b8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5b8-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de5b8-133">INPUTS</span></span>

### <span data-ttu-id="de5b8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="de5b8-134">System.String</span></span>

### <span data-ttu-id="de5b8-135">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="de5b8-135">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="de5b8-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de5b8-136">OUTPUTS</span></span>

### <span data-ttu-id="de5b8-137">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="de5b8-137">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="de5b8-138">Note</span><span class="sxs-lookup"><span data-stu-id="de5b8-138">NOTES</span></span>

## <span data-ttu-id="de5b8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de5b8-139">RELATED LINKS</span></span>
