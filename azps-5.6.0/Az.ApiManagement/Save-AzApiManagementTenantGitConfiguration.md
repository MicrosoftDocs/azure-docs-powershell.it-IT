---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: eb865535fcb4ee49b834e923fcf3f319ff5de074
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965518"
---
# <span data-ttu-id="bb20d-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb20d-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="bb20d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb20d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb20d-103">Salva le modifiche creando un commit per la configurazione corrente.</span><span class="sxs-lookup"><span data-stu-id="bb20d-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="bb20d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb20d-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb20d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb20d-105">DESCRIPTION</span></span>
<span data-ttu-id="bb20d-106">Il cmdlet **Save-AzApiManagementTenantGitConfiguration** salva le modifiche creando un commit che contiene lo snapshot di configurazione corrente in un ramo nel repository.</span><span class="sxs-lookup"><span data-stu-id="bb20d-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="bb20d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb20d-107">EXAMPLES</span></span>

### <span data-ttu-id="bb20d-108">Esempio 1: Salvare le modifiche alla configurazione</span><span class="sxs-lookup"><span data-stu-id="bb20d-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="bb20d-109">Questo comando salva le modifiche creando un commit con lo snapshot di configurazione corrente nel ramo specificato nel repository.</span><span class="sxs-lookup"><span data-stu-id="bb20d-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="bb20d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb20d-110">PARAMETERS</span></span>

### <span data-ttu-id="bb20d-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="bb20d-111">-Branch</span></span>
<span data-ttu-id="bb20d-112">Specifica il nome del ramo Git in cui eseguire il commit dello snapshot di configurazione corrente.</span><span class="sxs-lookup"><span data-stu-id="bb20d-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="bb20d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="bb20d-113">-Context</span></span>
<span data-ttu-id="bb20d-114">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="bb20d-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb20d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb20d-115">-DefaultProfile</span></span>
<span data-ttu-id="bb20d-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb20d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb20d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bb20d-117">-Force</span></span>
<span data-ttu-id="bb20d-118">Specifica che questo cmdlet esegue il commit del database di configurazione corrente nel repository Git, anche se il repository Git contiene modifiche più recenti che vengono sovrascritte.</span><span class="sxs-lookup"><span data-stu-id="bb20d-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb20d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb20d-119">-PassThru</span></span>
<span data-ttu-id="bb20d-120">Indica che questo cmdlet restituisce un **oggetto PsApiManagementOperationResult.**</span><span class="sxs-lookup"><span data-stu-id="bb20d-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb20d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb20d-121">-Confirm</span></span>
<span data-ttu-id="bb20d-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb20d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb20d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb20d-123">-WhatIf</span></span>
<span data-ttu-id="bb20d-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb20d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb20d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb20d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb20d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb20d-126">CommonParameters</span></span>
<span data-ttu-id="bb20d-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb20d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb20d-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb20d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb20d-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb20d-129">INPUTS</span></span>

### <span data-ttu-id="bb20d-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bb20d-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bb20d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bb20d-131">System.String</span></span>

### <span data-ttu-id="bb20d-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bb20d-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bb20d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb20d-133">OUTPUTS</span></span>

### <span data-ttu-id="bb20d-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="bb20d-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="bb20d-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb20d-135">NOTES</span></span>

## <span data-ttu-id="bb20d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb20d-136">RELATED LINKS</span></span>

[<span data-ttu-id="bb20d-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb20d-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


