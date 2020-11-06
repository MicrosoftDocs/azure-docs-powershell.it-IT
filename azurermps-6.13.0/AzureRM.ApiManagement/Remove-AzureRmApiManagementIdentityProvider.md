---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d8cc54570b1282889a93c803e1216096cde35b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507724"
---
# <span data-ttu-id="4ce91-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4ce91-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4ce91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ce91-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce91-103">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="4ce91-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ce91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ce91-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ce91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ce91-105">DESCRIPTION</span></span>
<span data-ttu-id="4ce91-106">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="4ce91-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="4ce91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ce91-107">EXAMPLES</span></span>

### <span data-ttu-id="4ce91-108">Rimuove le impostazioni del provider di identità di Facebook dal servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ce91-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="4ce91-109">Elimina la configurazione relativa alla configurazione del provider di identità di Facebook.</span><span class="sxs-lookup"><span data-stu-id="4ce91-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="4ce91-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ce91-110">PARAMETERS</span></span>

### <span data-ttu-id="4ce91-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4ce91-111">-Context</span></span>
<span data-ttu-id="4ce91-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4ce91-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4ce91-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4ce91-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4ce91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce91-114">-DefaultProfile</span></span>
<span data-ttu-id="4ce91-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce91-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ce91-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ce91-116">-PassThru</span></span>
<span data-ttu-id="4ce91-117">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4ce91-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="4ce91-118">-Digitare</span><span class="sxs-lookup"><span data-stu-id="4ce91-118">-Type</span></span>
<span data-ttu-id="4ce91-119">Identificatore di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="4ce91-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="4ce91-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4ce91-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce91-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ce91-121">-Confirm</span></span>
<span data-ttu-id="4ce91-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce91-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce91-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce91-123">-WhatIf</span></span>
<span data-ttu-id="4ce91-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ce91-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ce91-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ce91-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce91-126">CommonParameters</span></span>
<span data-ttu-id="4ce91-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ce91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce91-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce91-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce91-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ce91-129">INPUTS</span></span>

### <span data-ttu-id="4ce91-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4ce91-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4ce91-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="4ce91-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="4ce91-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ce91-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4ce91-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ce91-133">OUTPUTS</span></span>

### <span data-ttu-id="4ce91-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ce91-134">System.Boolean</span></span>

## <span data-ttu-id="4ce91-135">Note</span><span class="sxs-lookup"><span data-stu-id="4ce91-135">NOTES</span></span>

## <span data-ttu-id="4ce91-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ce91-136">RELATED LINKS</span></span>

[<span data-ttu-id="4ce91-137">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4ce91-137">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="4ce91-138">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4ce91-138">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="4ce91-139">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4ce91-139">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

