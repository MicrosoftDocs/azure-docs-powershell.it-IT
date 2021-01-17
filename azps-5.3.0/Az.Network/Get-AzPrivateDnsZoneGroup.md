---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488975"
---
# <span data-ttu-id="894bd-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="894bd-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="894bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="894bd-102">SYNOPSIS</span></span>
<span data-ttu-id="894bd-103">Ottiene il gruppo di aree DNS privato</span><span class="sxs-lookup"><span data-stu-id="894bd-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="894bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="894bd-104">SYNTAX</span></span>

### <span data-ttu-id="894bd-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="894bd-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="894bd-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="894bd-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="894bd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="894bd-107">DESCRIPTION</span></span>
<span data-ttu-id="894bd-108">Il cmdlet **Get-AzPrivateDnsZoneGroup** ottiene uno o più gruppi di aree DNS privati.</span><span class="sxs-lookup"><span data-stu-id="894bd-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="894bd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="894bd-109">EXAMPLES</span></span>

### <span data-ttu-id="894bd-110">Esempio 1: recuperare il gruppo di aree DNS private</span><span class="sxs-lookup"><span data-stu-id="894bd-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
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

<span data-ttu-id="894bd-111">Sopra l'esempio ottiene un gruppo di aree DNS privato denominato dnsgroup1 nel gruppo di risorse RG.</span><span class="sxs-lookup"><span data-stu-id="894bd-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="894bd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="894bd-112">PARAMETERS</span></span>

### <span data-ttu-id="894bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894bd-113">-DefaultProfile</span></span>
<span data-ttu-id="894bd-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="894bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="894bd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="894bd-115">-Name</span></span>
<span data-ttu-id="894bd-116">Nome del gruppo di aree private DNS.</span><span class="sxs-lookup"><span data-stu-id="894bd-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894bd-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="894bd-117">-PrivateEndpointName</span></span>
<span data-ttu-id="894bd-118">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="894bd-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="894bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="894bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="894bd-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="894bd-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="894bd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894bd-121">CommonParameters</span></span>
<span data-ttu-id="894bd-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894bd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894bd-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="894bd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894bd-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="894bd-124">INPUTS</span></span>

### <span data-ttu-id="894bd-125">System. String</span><span class="sxs-lookup"><span data-stu-id="894bd-125">System.String</span></span>

## <span data-ttu-id="894bd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="894bd-126">OUTPUTS</span></span>

### <span data-ttu-id="894bd-127">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="894bd-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="894bd-128">Note</span><span class="sxs-lookup"><span data-stu-id="894bd-128">NOTES</span></span>

## <span data-ttu-id="894bd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="894bd-129">RELATED LINKS</span></span>
