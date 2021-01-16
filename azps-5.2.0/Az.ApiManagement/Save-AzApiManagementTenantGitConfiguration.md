---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3995506c302d2993623f12fcb7e6e2b9f96fd208
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343936"
---
# <span data-ttu-id="c4b6c-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4b6c-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="c4b6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b6c-103">Consente di salvare le modifiche creando un commit per la configurazione corrente.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="c4b6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4b6c-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4b6c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="c4b6c-106">Il cmdlet **Save-AzApiManagementTenantGitConfiguration** Salva le modifiche creando un commit che contiene lo snapshot della configurazione corrente in un ramo del repository.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="c4b6c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4b6c-107">EXAMPLES</span></span>

### <span data-ttu-id="c4b6c-108">Esempio 1: salvare le modifiche apportate alla configurazione</span><span class="sxs-lookup"><span data-stu-id="c4b6c-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="c4b6c-109">Questo comando Salva le modifiche creando un commit con lo snapshot corrente della configurazione nella filiale specificata nel repository.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="c4b6c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4b6c-110">PARAMETERS</span></span>

### <span data-ttu-id="c4b6c-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="c4b6c-111">-Branch</span></span>
<span data-ttu-id="c4b6c-112">Specifica il nome del ramo git in cui eseguire il commit dello snapshot corrente della configurazione.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="c4b6c-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c4b6c-113">-Context</span></span>
<span data-ttu-id="c4b6c-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c4b6c-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c4b6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b6c-115">-DefaultProfile</span></span>
<span data-ttu-id="c4b6c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4b6c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c4b6c-117">-Force</span></span>
<span data-ttu-id="c4b6c-118">Specifica che questo cmdlet esegue il commit del database di configurazione corrente nel repository git, anche se il repository git contiene modifiche più recenti sovrascritte.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="c4b6c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4b6c-119">-PassThru</span></span>
<span data-ttu-id="c4b6c-120">Indica che questo cmdlet restituisce un oggetto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="c4b6c-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="c4b6c-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4b6c-121">-Confirm</span></span>
<span data-ttu-id="c4b6c-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4b6c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4b6c-123">-WhatIf</span></span>
<span data-ttu-id="c4b6c-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4b6c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4b6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b6c-126">CommonParameters</span></span>
<span data-ttu-id="c4b6c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4b6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b6c-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4b6c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b6c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4b6c-129">INPUTS</span></span>

### <span data-ttu-id="c4b6c-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c4b6c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c4b6c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c4b6c-131">System.String</span></span>

### <span data-ttu-id="c4b6c-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c4b6c-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c4b6c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4b6c-133">OUTPUTS</span></span>

### <span data-ttu-id="c4b6c-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="c4b6c-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="c4b6c-135">Note</span><span class="sxs-lookup"><span data-stu-id="c4b6c-135">NOTES</span></span>

## <span data-ttu-id="c4b6c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4b6c-136">RELATED LINKS</span></span>

[<span data-ttu-id="c4b6c-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4b6c-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


