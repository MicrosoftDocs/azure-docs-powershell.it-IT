---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/publish-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3879def437171e9de2cad6f328ef6bf15bed3d48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514568"
---
# <span data-ttu-id="be00b-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="be00b-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="be00b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be00b-102">SYNOPSIS</span></span>
<span data-ttu-id="be00b-103">Pubblica le modifiche da una filiale git al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="be00b-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be00b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be00b-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be00b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be00b-105">DESCRIPTION</span></span>
<span data-ttu-id="be00b-106">Il cmdlet **Publish-AzureRmApiManagementTenantGitConfiguration** pubblica le modifiche da una filiale git al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="be00b-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="be00b-107">In alternativa, è possibile convalidare le modifiche in un ramo git senza pubblicare.</span><span class="sxs-lookup"><span data-stu-id="be00b-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="be00b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be00b-108">EXAMPLES</span></span>

### <span data-ttu-id="be00b-109">Esempio 1: distribuire le modifiche git</span><span class="sxs-lookup"><span data-stu-id="be00b-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="be00b-110">Questo comando pubblica le modifiche dal ramo specificato al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="be00b-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="be00b-111">Esempio 2: convalidare le modifiche git</span><span class="sxs-lookup"><span data-stu-id="be00b-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="be00b-112">Questo comando Convalida le modifiche nel ramo git rispetto al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="be00b-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="be00b-113">Le modifiche non vengono pubblicate.</span><span class="sxs-lookup"><span data-stu-id="be00b-113">It does not publish changes.</span></span>

## <span data-ttu-id="be00b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be00b-114">PARAMETERS</span></span>

### <span data-ttu-id="be00b-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="be00b-115">-Branch</span></span>
<span data-ttu-id="be00b-116">Specifica il nome del ramo git da cui questo cmdlet distribuisce la configurazione al database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="be00b-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be00b-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="be00b-117">-Context</span></span>
<span data-ttu-id="be00b-118">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="be00b-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be00b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be00b-119">-DefaultProfile</span></span>
<span data-ttu-id="be00b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be00b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be00b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="be00b-121">-Force</span></span>
<span data-ttu-id="be00b-122">Indica che questo cmdlet elimina le sottoscrizioni ai prodotti eliminati in questo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="be00b-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be00b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be00b-123">-PassThru</span></span>
<span data-ttu-id="be00b-124">Indica che questo cmdlet restituisce un oggetto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="be00b-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be00b-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="be00b-125">-ValidateOnly</span></span>
<span data-ttu-id="be00b-126">Indica che questo cmdlet convalida le modifiche nel ramo git specificato.</span><span class="sxs-lookup"><span data-stu-id="be00b-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="be00b-127">Non viene pubblicata nel database di configurazione.</span><span class="sxs-lookup"><span data-stu-id="be00b-127">It does not publish to the configuration database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be00b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be00b-128">-Confirm</span></span>
<span data-ttu-id="be00b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be00b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be00b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be00b-130">-WhatIf</span></span>
<span data-ttu-id="be00b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be00b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be00b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be00b-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be00b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be00b-133">CommonParameters</span></span>
<span data-ttu-id="be00b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be00b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be00b-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be00b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be00b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be00b-136">INPUTS</span></span>

### <span data-ttu-id="be00b-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="be00b-137">None</span></span>
<span data-ttu-id="be00b-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="be00b-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be00b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be00b-139">OUTPUTS</span></span>

### <span data-ttu-id="be00b-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="be00b-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="be00b-141">Note</span><span class="sxs-lookup"><span data-stu-id="be00b-141">NOTES</span></span>

## <span data-ttu-id="be00b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be00b-142">RELATED LINKS</span></span>

[<span data-ttu-id="be00b-143">Salva-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="be00b-143">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


