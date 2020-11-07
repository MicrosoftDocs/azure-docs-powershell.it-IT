---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858589"
---
# <span data-ttu-id="21799-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="21799-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="21799-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21799-102">SYNOPSIS</span></span>
<span data-ttu-id="21799-103">Rimuove una regola di restrizione di Access da un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="21799-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="21799-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21799-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21799-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21799-105">DESCRIPTION</span></span>
<span data-ttu-id="21799-106">Il cmdlet **Remove-AzWebAppAccessRestrictionRule** rimuove una regola di restrizione di Access da un'app Web di Azure</span><span class="sxs-lookup"><span data-stu-id="21799-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="21799-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21799-107">EXAMPLES</span></span>

### <span data-ttu-id="21799-108">Esempio 1: rimuovere una regola di restrizione di Access per l'app Web</span><span class="sxs-lookup"><span data-stu-id="21799-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="21799-109">Questo comando rimuove la regola di restrizione di accesso di IpRule da Azure Web App denominata ContosoSite che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="21799-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="21799-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21799-110">PARAMETERS</span></span>

### <span data-ttu-id="21799-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21799-111">-DefaultProfile</span></span>
<span data-ttu-id="21799-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21799-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21799-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="21799-113">-Name</span></span>
<span data-ttu-id="21799-114">Nome della regola di restrizione di Access</span><span class="sxs-lookup"><span data-stu-id="21799-114">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="21799-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21799-115">-PassThru</span></span>
<span data-ttu-id="21799-116">Restituisce l'oggetto di configurazione di restrizione di Access.</span><span class="sxs-lookup"><span data-stu-id="21799-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="21799-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21799-117">-ResourceGroupName</span></span>
<span data-ttu-id="21799-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="21799-118">Resource Group Name</span></span>

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

### <span data-ttu-id="21799-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="21799-119">-SlotName</span></span>
<span data-ttu-id="21799-120">Nome dello slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="21799-120">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="21799-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="21799-121">-TargetScmSite</span></span>
<span data-ttu-id="21799-122">La regola è destinata al sito principale o all'area SCM.</span><span class="sxs-lookup"><span data-stu-id="21799-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="21799-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="21799-123">-WebAppName</span></span>
<span data-ttu-id="21799-124">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="21799-124">The name of the web app.</span></span>

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

### <span data-ttu-id="21799-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21799-125">-Confirm</span></span>
<span data-ttu-id="21799-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21799-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21799-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21799-127">-WhatIf</span></span>
<span data-ttu-id="21799-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21799-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21799-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21799-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21799-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21799-130">CommonParameters</span></span>
<span data-ttu-id="21799-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21799-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21799-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21799-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21799-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21799-133">INPUTS</span></span>

### <span data-ttu-id="21799-134">System. String</span><span class="sxs-lookup"><span data-stu-id="21799-134">System.String</span></span>

## <span data-ttu-id="21799-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21799-135">OUTPUTS</span></span>

### <span data-ttu-id="21799-136">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="21799-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="21799-137">Note</span><span class="sxs-lookup"><span data-stu-id="21799-137">NOTES</span></span>

## <span data-ttu-id="21799-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21799-138">RELATED LINKS</span></span>

[<span data-ttu-id="21799-139">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="21799-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="21799-140">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="21799-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="21799-141">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="21799-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
