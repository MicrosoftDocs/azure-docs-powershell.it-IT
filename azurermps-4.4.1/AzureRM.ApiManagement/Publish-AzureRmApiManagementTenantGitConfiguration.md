---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 2a867109bf44cd652eaf1d256d963796e06762cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510787"
---
# <span data-ttu-id="6ac13-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ac13-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="6ac13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ac13-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac13-103">Pubblica le modifiche da una filiale git al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6ac13-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ac13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ac13-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ac13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ac13-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac13-106">Il cmdlet **Publish-AzureRmApiManagementTenantGitConfiguration** pubblica le modifiche da una filiale git al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6ac13-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="6ac13-107">In alternativa, è possibile convalidare le modifiche in un ramo git senza pubblicare.</span><span class="sxs-lookup"><span data-stu-id="6ac13-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="6ac13-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ac13-108">EXAMPLES</span></span>

### <span data-ttu-id="6ac13-109">Esempio 1: distribuire le modifiche git</span><span class="sxs-lookup"><span data-stu-id="6ac13-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="6ac13-110">Questo comando pubblica le modifiche dal ramo specificato al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6ac13-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="6ac13-111">Esempio 2: convalidare le modifiche git</span><span class="sxs-lookup"><span data-stu-id="6ac13-111">Example 2: Validate Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="6ac13-112">Questo comando Convalida le modifiche nel ramo git rispetto al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6ac13-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="6ac13-113">Le modifiche non vengono pubblicate.</span><span class="sxs-lookup"><span data-stu-id="6ac13-113">It does not publish changes.</span></span>

## <span data-ttu-id="6ac13-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ac13-114">PARAMETERS</span></span>

### <span data-ttu-id="6ac13-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="6ac13-115">-Branch</span></span>
<span data-ttu-id="6ac13-116">Specifica il nome del ramo git da cui questo cmdlet distribuisce la configurazione al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6ac13-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="6ac13-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6ac13-117">-Context</span></span>
<span data-ttu-id="6ac13-118">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6ac13-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6ac13-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6ac13-119">-Force</span></span>
<span data-ttu-id="6ac13-120">Indica che questo cmdlet elimina le sottoscrizioni ai prodotti eliminati in questo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6ac13-120">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="6ac13-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ac13-121">-PassThru</span></span>
<span data-ttu-id="6ac13-122">Indica che questo cmdlet restituisce un oggetto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="6ac13-122">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="6ac13-123">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="6ac13-123">-ValidateOnly</span></span>
<span data-ttu-id="6ac13-124">Indica che questo cmdlet convalida le modifiche nel ramo git specificato.</span><span class="sxs-lookup"><span data-stu-id="6ac13-124">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="6ac13-125">Non viene pubblicata nel database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6ac13-125">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="6ac13-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ac13-126">-Confirm</span></span>
<span data-ttu-id="6ac13-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ac13-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ac13-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ac13-128">-WhatIf</span></span>
<span data-ttu-id="6ac13-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ac13-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ac13-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ac13-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ac13-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac13-131">-DefaultProfile</span></span>
<span data-ttu-id="6ac13-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ac13-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ac13-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac13-133">CommonParameters</span></span>
<span data-ttu-id="6ac13-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ac13-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac13-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac13-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac13-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ac13-136">INPUTS</span></span>

## <span data-ttu-id="6ac13-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ac13-137">OUTPUTS</span></span>

### <span data-ttu-id="6ac13-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="6ac13-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="6ac13-139">Note</span><span class="sxs-lookup"><span data-stu-id="6ac13-139">NOTES</span></span>

## <span data-ttu-id="6ac13-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ac13-140">RELATED LINKS</span></span>

[<span data-ttu-id="6ac13-141">Salva-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ac13-141">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


