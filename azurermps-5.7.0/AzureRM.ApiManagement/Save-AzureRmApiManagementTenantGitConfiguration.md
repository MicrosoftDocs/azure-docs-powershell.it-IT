---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/save-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 7401c359a9af82d1b65749a3276aada89ab9320d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508420"
---
# <span data-ttu-id="2de9d-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="2de9d-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="2de9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2de9d-102">SYNOPSIS</span></span>
<span data-ttu-id="2de9d-103">Consente di salvare le modifiche creando un commit per la configurazione corrente.</span><span class="sxs-lookup"><span data-stu-id="2de9d-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2de9d-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2de9d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2de9d-105">DESCRIPTION</span></span>
<span data-ttu-id="2de9d-106">Il cmdlet **Save-AzureRmApiManagementTenantGitConfiguration** Salva le modifiche creando un commit che contiene lo snapshot della configurazione corrente in un ramo del repository.</span><span class="sxs-lookup"><span data-stu-id="2de9d-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="2de9d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2de9d-107">EXAMPLES</span></span>

### <span data-ttu-id="2de9d-108">Esempio 1: salvare le modifiche apportate alla configurazione</span><span class="sxs-lookup"><span data-stu-id="2de9d-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="2de9d-109">Questo comando Salva le modifiche creando un commit con lo snapshot corrente della configurazione nella filiale specificata nel repository.</span><span class="sxs-lookup"><span data-stu-id="2de9d-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="2de9d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2de9d-110">PARAMETERS</span></span>

### <span data-ttu-id="2de9d-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="2de9d-111">-Branch</span></span>
<span data-ttu-id="2de9d-112">Specifica il nome del ramo git in cui eseguire il commit dello snapshot corrente della configurazione.</span><span class="sxs-lookup"><span data-stu-id="2de9d-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="2de9d-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2de9d-113">-Context</span></span>
<span data-ttu-id="2de9d-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2de9d-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2de9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de9d-115">-DefaultProfile</span></span>
<span data-ttu-id="2de9d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2de9d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2de9d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2de9d-117">-Force</span></span>
<span data-ttu-id="2de9d-118">Specifica che questo cmdlet esegue il commit del database di configurazione corrente nel repository git, anche se il repository git contiene modifiche più recenti sovrascritte.</span><span class="sxs-lookup"><span data-stu-id="2de9d-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="2de9d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2de9d-119">-PassThru</span></span>
<span data-ttu-id="2de9d-120">Indica che questo cmdlet restituisce un oggetto **PsApiManagementOperationResult** .</span><span class="sxs-lookup"><span data-stu-id="2de9d-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="2de9d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2de9d-121">-Confirm</span></span>
<span data-ttu-id="2de9d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2de9d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de9d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de9d-123">-WhatIf</span></span>
<span data-ttu-id="2de9d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2de9d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de9d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2de9d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de9d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de9d-126">CommonParameters</span></span>
<span data-ttu-id="2de9d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de9d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de9d-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de9d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de9d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2de9d-129">INPUTS</span></span>

### <span data-ttu-id="2de9d-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2de9d-130">None</span></span>
<span data-ttu-id="2de9d-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="2de9d-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2de9d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2de9d-132">OUTPUTS</span></span>

### <span data-ttu-id="2de9d-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="2de9d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="2de9d-134">Note</span><span class="sxs-lookup"><span data-stu-id="2de9d-134">NOTES</span></span>

## <span data-ttu-id="2de9d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2de9d-135">RELATED LINKS</span></span>

[<span data-ttu-id="2de9d-136">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="2de9d-136">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


