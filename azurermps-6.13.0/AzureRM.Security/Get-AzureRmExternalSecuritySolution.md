---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmExternalSecuritySolution.md
ms.openlocfilehash: 4ef54651b5490161d7fc28c4a0c068f7b4a1ed76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519219"
---
# <span data-ttu-id="729bd-101">Get-AzureRmExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="729bd-101">Get-AzureRmExternalSecuritySolution</span></span>

## <span data-ttu-id="729bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="729bd-102">SYNOPSIS</span></span>
<span data-ttu-id="729bd-103">Ottenere una soluzione di sicurezza esterna</span><span class="sxs-lookup"><span data-stu-id="729bd-103">Get external security solution</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="729bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="729bd-104">SYNTAX</span></span>

### <span data-ttu-id="729bd-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="729bd-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="729bd-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="729bd-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="729bd-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="729bd-107">SubscriptionLevelResource</span></span>
```
Get-AzureRmExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="729bd-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="729bd-108">ResourceId</span></span>
```
Get-AzureRmExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="729bd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="729bd-109">DESCRIPTION</span></span>
<span data-ttu-id="729bd-110">Ottenere una soluzione di sicurezza esterna</span><span class="sxs-lookup"><span data-stu-id="729bd-110">Get external security solution</span></span>

## <span data-ttu-id="729bd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="729bd-111">EXAMPLES</span></span>

### <span data-ttu-id="729bd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="729bd-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="729bd-113">Ottenere tutte le soluzioni di sicurezza esterna nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="729bd-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="729bd-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="729bd-114">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="729bd-115">Ottenere una soluzione di sicurezza esterna specifica</span><span class="sxs-lookup"><span data-stu-id="729bd-115">Get a specific external security solution</span></span>

## <span data-ttu-id="729bd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="729bd-116">PARAMETERS</span></span>

### <span data-ttu-id="729bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729bd-117">-DefaultProfile</span></span>
<span data-ttu-id="729bd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="729bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729bd-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="729bd-119">-Location</span></span>
<span data-ttu-id="729bd-120">Posizione.</span><span class="sxs-lookup"><span data-stu-id="729bd-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729bd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="729bd-121">-Name</span></span>
<span data-ttu-id="729bd-122">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="729bd-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729bd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="729bd-123">-ResourceGroupName</span></span>
<span data-ttu-id="729bd-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="729bd-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="729bd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="729bd-125">-ResourceId</span></span>
<span data-ttu-id="729bd-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="729bd-126">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="729bd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729bd-127">CommonParameters</span></span>
<span data-ttu-id="729bd-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="729bd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729bd-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="729bd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729bd-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="729bd-130">INPUTS</span></span>

### <span data-ttu-id="729bd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="729bd-131">System.String</span></span>

## <span data-ttu-id="729bd-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="729bd-132">OUTPUTS</span></span>

### <span data-ttu-id="729bd-133">Microsoft. Azure. Commands. Security. Models. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="729bd-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="729bd-134">Note</span><span class="sxs-lookup"><span data-stu-id="729bd-134">NOTES</span></span>

## <span data-ttu-id="729bd-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="729bd-135">RELATED LINKS</span></span>
