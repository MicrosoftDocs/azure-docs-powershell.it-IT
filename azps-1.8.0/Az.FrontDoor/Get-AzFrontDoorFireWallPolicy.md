---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 5933d860ca2badce2d9576409dd1553153bb1e84
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401505"
---
# <span data-ttu-id="02a3f-101">Get-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="02a3f-101">Get-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="02a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="02a3f-103">Ottenere i criteri WAF</span><span class="sxs-lookup"><span data-stu-id="02a3f-103">Get WAF policy</span></span>

## <span data-ttu-id="02a3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02a3f-104">SYNTAX</span></span>

```
Get-AzFrontDoorFireWallPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02a3f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="02a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="02a3f-106">Il **cmdlet Get-AzFrontDoorFireWallPolicyGet** ottiene i criteri WAF in un gruppo di risorse nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="02a3f-106">The **Get-AzFrontDoorFireWallPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="02a3f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02a3f-107">EXAMPLES</span></span>

### <span data-ttu-id="02a3f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02a3f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="02a3f-109">Ottenere un criterio WAF denominato $policyName in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a3f-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="02a3f-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="02a3f-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="02a3f-111">Ottenere tutti i criteri WAF in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a3f-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="02a3f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02a3f-112">PARAMETERS</span></span>

### <span data-ttu-id="02a3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a3f-113">-DefaultProfile</span></span>
<span data-ttu-id="02a3f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02a3f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a3f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="02a3f-115">-Name</span></span>
<span data-ttu-id="02a3f-116">Nome FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="02a3f-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="02a3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="02a3f-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="02a3f-118">The resource group name.</span></span>

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

### <span data-ttu-id="02a3f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a3f-119">CommonParameters</span></span>
<span data-ttu-id="02a3f-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a3f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a3f-121">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="02a3f-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a3f-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="02a3f-122">INPUTS</span></span>

### <span data-ttu-id="02a3f-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="02a3f-123">None</span></span>

## <span data-ttu-id="02a3f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02a3f-124">OUTPUTS</span></span>

### <span data-ttu-id="02a3f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="02a3f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="02a3f-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="02a3f-126">NOTES</span></span>

## <span data-ttu-id="02a3f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02a3f-127">RELATED LINKS</span></span>

<span data-ttu-id="02a3f-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="02a3f-128">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)</span></span>
