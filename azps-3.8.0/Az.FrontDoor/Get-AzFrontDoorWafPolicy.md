---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: daf4631041093b10a1bf712649de8b5c3ad3b6d9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404021"
---
# <span data-ttu-id="04109-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="04109-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="04109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04109-102">SYNOPSIS</span></span>
<span data-ttu-id="04109-103">Ottenere i criteri WAF</span><span class="sxs-lookup"><span data-stu-id="04109-103">Get WAF policy</span></span>

## <span data-ttu-id="04109-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04109-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04109-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="04109-105">DESCRIPTION</span></span>
<span data-ttu-id="04109-106">Il **cmdlet Get-AzFrontDoorWafPolicyGet** ottiene i criteri WAF in un gruppo di risorse nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="04109-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="04109-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04109-107">EXAMPLES</span></span>

### <span data-ttu-id="04109-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04109-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="04109-109">Ottenere un criterio WAF denominato $policyName in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04109-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="04109-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="04109-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="04109-111">Ottenere tutti i criteri WAF in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04109-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="04109-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04109-112">PARAMETERS</span></span>

### <span data-ttu-id="04109-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04109-113">-DefaultProfile</span></span>
<span data-ttu-id="04109-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04109-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04109-115">-Name</span><span class="sxs-lookup"><span data-stu-id="04109-115">-Name</span></span>
<span data-ttu-id="04109-116">Nome FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="04109-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="04109-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04109-117">-ResourceGroupName</span></span>
<span data-ttu-id="04109-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="04109-118">The resource group name.</span></span>

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

### <span data-ttu-id="04109-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04109-119">CommonParameters</span></span>
<span data-ttu-id="04109-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04109-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04109-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04109-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04109-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="04109-122">INPUTS</span></span>

### <span data-ttu-id="04109-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="04109-123">None</span></span>

## <span data-ttu-id="04109-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04109-124">OUTPUTS</span></span>

### <span data-ttu-id="04109-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="04109-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="04109-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="04109-126">NOTES</span></span>

## <span data-ttu-id="04109-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04109-127">RELATED LINKS</span></span>

<span data-ttu-id="04109-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="04109-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
