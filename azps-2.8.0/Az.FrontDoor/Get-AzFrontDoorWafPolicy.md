---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 5cc2a2e480044aa00c51a18dd116d33bd4c2f72a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398462"
---
# <span data-ttu-id="8d006-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="8d006-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="8d006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d006-102">SYNOPSIS</span></span>
<span data-ttu-id="8d006-103">Ottenere i criteri WAF</span><span class="sxs-lookup"><span data-stu-id="8d006-103">Get WAF policy</span></span>

## <span data-ttu-id="8d006-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d006-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d006-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d006-105">DESCRIPTION</span></span>
<span data-ttu-id="8d006-106">Il **cmdlet Get-AzFrontDoorWafPolicyGet** ottiene i criteri WAF in un gruppo di risorse nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="8d006-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="8d006-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d006-107">EXAMPLES</span></span>

### <span data-ttu-id="8d006-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8d006-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="8d006-109">Ottenere un criterio WAF denominato $policyName in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d006-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="8d006-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8d006-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="8d006-111">Ottenere tutti i criteri WAF in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d006-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="8d006-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d006-112">PARAMETERS</span></span>

### <span data-ttu-id="8d006-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d006-113">-DefaultProfile</span></span>
<span data-ttu-id="8d006-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d006-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d006-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8d006-115">-Name</span></span>
<span data-ttu-id="8d006-116">Nome FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="8d006-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="8d006-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d006-117">-ResourceGroupName</span></span>
<span data-ttu-id="8d006-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8d006-118">The resource group name.</span></span>

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

### <span data-ttu-id="8d006-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d006-119">CommonParameters</span></span>
<span data-ttu-id="8d006-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d006-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d006-121">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d006-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d006-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d006-122">INPUTS</span></span>

### <span data-ttu-id="8d006-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8d006-123">None</span></span>

## <span data-ttu-id="8d006-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d006-124">OUTPUTS</span></span>

### <span data-ttu-id="8d006-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8d006-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="8d006-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d006-126">NOTES</span></span>

## <span data-ttu-id="8d006-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d006-127">RELATED LINKS</span></span>

<span data-ttu-id="8d006-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="8d006-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
