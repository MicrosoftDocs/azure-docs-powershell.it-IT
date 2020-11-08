---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: e15e6757d6a4d0f6e84a9580877deecdeede94ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032005"
---
# <span data-ttu-id="4ad14-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4ad14-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4ad14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ad14-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad14-103">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="4ad14-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="4ad14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ad14-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ad14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ad14-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad14-106">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="4ad14-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="4ad14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ad14-107">EXAMPLES</span></span>

### <span data-ttu-id="4ad14-108">Esempio 1: rimuove le impostazioni del provider di identità di Facebook dal servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ad14-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="4ad14-109">Elimina la configurazione relativa alla configurazione del provider di identità di Facebook.</span><span class="sxs-lookup"><span data-stu-id="4ad14-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="4ad14-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ad14-110">PARAMETERS</span></span>

### <span data-ttu-id="4ad14-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4ad14-111">-Context</span></span>
<span data-ttu-id="4ad14-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4ad14-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4ad14-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4ad14-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4ad14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad14-114">-DefaultProfile</span></span>
<span data-ttu-id="4ad14-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad14-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ad14-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ad14-116">-PassThru</span></span>
<span data-ttu-id="4ad14-117">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4ad14-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="4ad14-118">-Digitare</span><span class="sxs-lookup"><span data-stu-id="4ad14-118">-Type</span></span>
<span data-ttu-id="4ad14-119">Identificatore di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="4ad14-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="4ad14-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4ad14-120">This parameter is required.</span></span>

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

### <span data-ttu-id="4ad14-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ad14-121">-Confirm</span></span>
<span data-ttu-id="4ad14-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad14-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad14-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad14-123">-WhatIf</span></span>
<span data-ttu-id="4ad14-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ad14-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ad14-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ad14-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad14-126">CommonParameters</span></span>
<span data-ttu-id="4ad14-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad14-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ad14-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad14-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ad14-129">INPUTS</span></span>

### <span data-ttu-id="4ad14-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4ad14-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4ad14-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="4ad14-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="4ad14-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ad14-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4ad14-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ad14-133">OUTPUTS</span></span>

### <span data-ttu-id="4ad14-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ad14-134">System.Boolean</span></span>

## <span data-ttu-id="4ad14-135">Note</span><span class="sxs-lookup"><span data-stu-id="4ad14-135">NOTES</span></span>

## <span data-ttu-id="4ad14-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ad14-136">RELATED LINKS</span></span>

[<span data-ttu-id="4ad14-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4ad14-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="4ad14-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4ad14-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="4ad14-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4ad14-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

