---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 283bc1a14404c842da0ed99e43596984b1559299
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518660"
---
# <span data-ttu-id="67dc3-101">Get-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="67dc3-101">Get-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="67dc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="67dc3-103">Ottenere i criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="67dc3-103">Get WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67dc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67dc3-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67dc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="67dc3-106">Il **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet ottiene i criteri di WAF in un gruppo di risorse sotto l'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="67dc3-106">The **Get-AzureRmFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="67dc3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67dc3-107">EXAMPLES</span></span>

### <span data-ttu-id="67dc3-108">Esempio 1: ottenere un criterio WAF denominato $Name in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="67dc3-108">Example 1: Get a WAF policy called $Name in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="67dc3-109">Ottenere un criterio WAF denominato $Name in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="67dc3-109">Get a WAF policy called $Name in $resourceGroup</span></span>

### <span data-ttu-id="67dc3-110">Esempio 2: ottenere tutti i criteri di WAF in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="67dc3-110">Example 2: Get all WAF policy in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name1}
Name               : {Name1}
Type               :

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name2}
Name               : {Name2}
Type               :
```

<span data-ttu-id="67dc3-111">Ottenere tutti i criteri di WAF in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="67dc3-111">Get all WAF policy in $resourceGroup</span></span>

## <span data-ttu-id="67dc3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67dc3-112">PARAMETERS</span></span>

### <span data-ttu-id="67dc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67dc3-113">-DefaultProfile</span></span>
<span data-ttu-id="67dc3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67dc3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67dc3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="67dc3-115">-Name</span></span>
<span data-ttu-id="67dc3-116">Nome FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="67dc3-116">FireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67dc3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67dc3-117">-ResourceGroupName</span></span>
<span data-ttu-id="67dc3-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67dc3-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67dc3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67dc3-119">CommonParameters</span></span>
<span data-ttu-id="67dc3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67dc3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67dc3-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67dc3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67dc3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67dc3-122">INPUTS</span></span>

### <span data-ttu-id="67dc3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="67dc3-123">System.String</span></span>

## <span data-ttu-id="67dc3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67dc3-124">OUTPUTS</span></span>

### <span data-ttu-id="67dc3-125">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="67dc3-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="67dc3-126">Note</span><span class="sxs-lookup"><span data-stu-id="67dc3-126">NOTES</span></span>

## <span data-ttu-id="67dc3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67dc3-127">RELATED LINKS</span></span>

<span data-ttu-id="67dc3-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="67dc3-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)</span></span>
