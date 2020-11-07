---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: b9963fc53a146a2e8c76ac9b15166f0de6ba67ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675971"
---
# <span data-ttu-id="2d667-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d667-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="2d667-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d667-102">SYNOPSIS</span></span>
<span data-ttu-id="2d667-103">Pubblica le modifiche da una filiale git al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2d667-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="2d667-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d667-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d667-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d667-105">DESCRIPTION</span></span>
<span data-ttu-id="2d667-106">Il cmdlet **Publish-AzApiManagementTenantGitConfiguration** pubblica le modifiche da una filiale git al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2d667-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="2d667-107">In alternativa, è possibile convalidare le modifiche in un ramo git senza pubblicare.</span><span class="sxs-lookup"><span data-stu-id="2d667-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="2d667-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d667-108">EXAMPLES</span></span>

### <span data-ttu-id="2d667-109">Esempio 1: distribuire le modifiche git</span><span class="sxs-lookup"><span data-stu-id="2d667-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="2d667-110">Questo comando pubblica le modifiche dal ramo specificato al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2d667-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="2d667-111">Esempio 2: convalidare le modifiche git</span><span class="sxs-lookup"><span data-stu-id="2d667-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="2d667-112">Questo comando Convalida le modifiche nel ramo git rispetto al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2d667-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="2d667-113">Le modifiche non vengono pubblicate.</span><span class="sxs-lookup"><span data-stu-id="2d667-113">It does not publish changes.</span></span>

## <span data-ttu-id="2d667-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d667-114">PARAMETERS</span></span>

### <span data-ttu-id="2d667-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="2d667-115">-Branch</span></span>
<span data-ttu-id="2d667-116">Specifica il nome del ramo git da cui questo cmdlet distribuisce la configurazione al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2d667-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="2d667-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2d667-117">-Context</span></span>
<span data-ttu-id="2d667-118">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2d667-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d667-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d667-119">-DefaultProfile</span></span>
<span data-ttu-id="2d667-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d667-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d667-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2d667-121">-Force</span></span>
<span data-ttu-id="2d667-122">Indica che questo cmdlet elimina le sottoscrizioni ai prodotti eliminati in questo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2d667-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="2d667-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d667-123">-PassThru</span></span>
<span data-ttu-id="2d667-124">Indica che questo cmdlet restituisce un oggetto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="2d667-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="2d667-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="2d667-125">-ValidateOnly</span></span>
<span data-ttu-id="2d667-126">Indica che questo cmdlet convalida le modifiche nel ramo git specificato.</span><span class="sxs-lookup"><span data-stu-id="2d667-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="2d667-127">Non viene pubblicata nel database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2d667-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="2d667-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d667-128">-Confirm</span></span>
<span data-ttu-id="2d667-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d667-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d667-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d667-130">-WhatIf</span></span>
<span data-ttu-id="2d667-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d667-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d667-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d667-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d667-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d667-133">CommonParameters</span></span>
<span data-ttu-id="2d667-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d667-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d667-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d667-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d667-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d667-136">INPUTS</span></span>

### <span data-ttu-id="2d667-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2d667-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2d667-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2d667-138">System.String</span></span>

### <span data-ttu-id="2d667-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2d667-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2d667-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d667-140">OUTPUTS</span></span>

### <span data-ttu-id="2d667-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="2d667-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="2d667-142">Note</span><span class="sxs-lookup"><span data-stu-id="2d667-142">NOTES</span></span>

## <span data-ttu-id="2d667-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d667-143">RELATED LINKS</span></span>

[<span data-ttu-id="2d667-144">Salva-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d667-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


