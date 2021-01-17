---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ea1ace189271c96bbf4bda0bc67385c678ef3c40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350236"
---
# <span data-ttu-id="07815-101">Get-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="07815-101">Get-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="07815-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07815-102">SYNOPSIS</span></span>
<span data-ttu-id="07815-103">Ottenere i criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="07815-103">Get WAF policy</span></span>

## <span data-ttu-id="07815-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07815-104">SYNTAX</span></span>

```
Get-AzFrontDoorWafPolicy -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07815-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07815-105">DESCRIPTION</span></span>
<span data-ttu-id="07815-106">Il **Get-AzFrontDoorWafPolicy** cmdletGet ottiene i criteri di WAF in un gruppo di risorse sotto l'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="07815-106">The **Get-AzFrontDoorWafPolicy** cmdletGet gets WAF policy in a resource group under the current subscription</span></span>

## <span data-ttu-id="07815-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07815-107">EXAMPLES</span></span>

### <span data-ttu-id="07815-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07815-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="07815-109">Ottenere un criterio WAF denominato $policyName in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07815-109">Get a WAF policy called $policyName in $resourceGroupName</span></span>

### <span data-ttu-id="07815-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="07815-110">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention           Disabled
{policyName} Detection             Enabled                           403 https://www.bing.com/
{policyName} Detection             Enabled                           404
```

<span data-ttu-id="07815-111">Ottenere tutti i criteri di WAF in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07815-111">Get all WAF policy in $resourceGroupName</span></span>

## <span data-ttu-id="07815-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07815-112">PARAMETERS</span></span>

### <span data-ttu-id="07815-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07815-113">-DefaultProfile</span></span>
<span data-ttu-id="07815-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07815-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07815-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="07815-115">-Name</span></span>
<span data-ttu-id="07815-116">Nome FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="07815-116">FireWallPolicy name.</span></span>

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

### <span data-ttu-id="07815-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07815-117">-ResourceGroupName</span></span>
<span data-ttu-id="07815-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07815-118">The resource group name.</span></span>

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

### <span data-ttu-id="07815-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07815-119">CommonParameters</span></span>
<span data-ttu-id="07815-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07815-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07815-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07815-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07815-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07815-122">INPUTS</span></span>

### <span data-ttu-id="07815-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="07815-123">None</span></span>

## <span data-ttu-id="07815-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07815-124">OUTPUTS</span></span>

### <span data-ttu-id="07815-125">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="07815-125">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="07815-126">Note</span><span class="sxs-lookup"><span data-stu-id="07815-126">NOTES</span></span>

## <span data-ttu-id="07815-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07815-127">RELATED LINKS</span></span>

<span data-ttu-id="07815-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="07815-128">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)</span></span>
