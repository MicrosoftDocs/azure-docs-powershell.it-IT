---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326911"
---
# <span data-ttu-id="dd0e8-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="dd0e8-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="dd0e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0e8-103">Ottiene la configurazione di restiction di Access per una Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dd0e8-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="dd0e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd0e8-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd0e8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd0e8-105">DESCRIPTION</span></span>
<span data-ttu-id="dd0e8-106">Il cmdlet **Get-AzWebAppAccessRestrictionConfig** ottiene la configurazione della restrizione di Access su una Web App Azure.</span><span class="sxs-lookup"><span data-stu-id="dd0e8-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="dd0e8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd0e8-107">EXAMPLES</span></span>

### <span data-ttu-id="dd0e8-108">Esempio 1: ottenere una configurazione di restrizione di accesso alle app Web da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="dd0e8-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="dd0e8-109">Questo comando ottiene la configurazione di restrizione di Access di un'app Web denominata ContosoSite che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="dd0e8-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="dd0e8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd0e8-110">PARAMETERS</span></span>

### <span data-ttu-id="dd0e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd0e8-111">-DefaultProfile</span></span>
<span data-ttu-id="dd0e8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd0e8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd0e8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd0e8-113">-Name</span></span>
<span data-ttu-id="dd0e8-114">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="dd0e8-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd0e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd0e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="dd0e8-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="dd0e8-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd0e8-117">-Slotname</span><span class="sxs-lookup"><span data-stu-id="dd0e8-117">-SlotName</span></span>
<span data-ttu-id="dd0e8-118">Nome dello slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="dd0e8-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd0e8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0e8-119">CommonParameters</span></span>
<span data-ttu-id="dd0e8-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd0e8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0e8-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd0e8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0e8-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd0e8-122">INPUTS</span></span>

### <span data-ttu-id="dd0e8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dd0e8-123">System.String</span></span>

## <span data-ttu-id="dd0e8-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd0e8-124">OUTPUTS</span></span>

### <span data-ttu-id="dd0e8-125">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="dd0e8-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="dd0e8-126">Note</span><span class="sxs-lookup"><span data-stu-id="dd0e8-126">NOTES</span></span>

## <span data-ttu-id="dd0e8-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd0e8-127">RELATED LINKS</span></span>

[<span data-ttu-id="dd0e8-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="dd0e8-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="dd0e8-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="dd0e8-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="dd0e8-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="dd0e8-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
