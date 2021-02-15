---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193751"
---
# <span data-ttu-id="4d4f9-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4d4f9-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="4d4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4f9-103">Ottiene il gruppo di zona DNS privato</span><span class="sxs-lookup"><span data-stu-id="4d4f9-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="4d4f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d4f9-104">SYNTAX</span></span>

### <span data-ttu-id="4d4f9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d4f9-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d4f9-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="4d4f9-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d4f9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d4f9-107">DESCRIPTION</span></span>
<span data-ttu-id="4d4f9-108">Il cmdlet **Get-AzPrivateDnsZoneGroup** ottiene uno o più gruppi di zona DNS privati.</span><span class="sxs-lookup"><span data-stu-id="4d4f9-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="4d4f9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d4f9-109">EXAMPLES</span></span>

### <span data-ttu-id="4d4f9-110">Esempio 1: Recuperare un gruppo di zona DNS privato</span><span class="sxs-lookup"><span data-stu-id="4d4f9-110">Example 1: Retrieve private DNS zone group</span></span>
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

<span data-ttu-id="4d4f9-111">L'esempio precedente recupera un gruppo di zona DNS privato denominato dnsgroup1 nel gruppo di risorse rg.</span><span class="sxs-lookup"><span data-stu-id="4d4f9-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="4d4f9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d4f9-112">PARAMETERS</span></span>

### <span data-ttu-id="4d4f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4f9-113">-DefaultProfile</span></span>
<span data-ttu-id="4d4f9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d4f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d4f9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4d4f9-115">-Name</span></span>
<span data-ttu-id="4d4f9-116">Nome del gruppo di zona DNS privato.</span><span class="sxs-lookup"><span data-stu-id="4d4f9-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="4d4f9-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="4d4f9-117">-PrivateEndpointName</span></span>
<span data-ttu-id="4d4f9-118">Nome dell'endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="4d4f9-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="4d4f9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4f9-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d4f9-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d4f9-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d4f9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4f9-121">CommonParameters</span></span>
<span data-ttu-id="4d4f9-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d4f9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4f9-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d4f9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4f9-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d4f9-124">INPUTS</span></span>

### <span data-ttu-id="4d4f9-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4d4f9-125">System.String</span></span>

## <span data-ttu-id="4d4f9-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d4f9-126">OUTPUTS</span></span>

### <span data-ttu-id="4d4f9-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="4d4f9-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="4d4f9-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d4f9-128">NOTES</span></span>

## <span data-ttu-id="4d4f9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d4f9-129">RELATED LINKS</span></span>
