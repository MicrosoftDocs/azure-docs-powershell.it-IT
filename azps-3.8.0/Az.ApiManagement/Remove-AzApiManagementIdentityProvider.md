---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 4909c9d9b9a7fa1af1e4353c63256ed73d229f57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020112"
---
# <span data-ttu-id="45312-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="45312-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="45312-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45312-102">SYNOPSIS</span></span>
<span data-ttu-id="45312-103">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="45312-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="45312-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45312-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45312-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45312-105">DESCRIPTION</span></span>
<span data-ttu-id="45312-106">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="45312-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="45312-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45312-107">EXAMPLES</span></span>

### <span data-ttu-id="45312-108">Rimuove le impostazioni del provider di identità di Facebook dal servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45312-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="45312-109">Elimina la configurazione relativa alla configurazione del provider di identità di Facebook.</span><span class="sxs-lookup"><span data-stu-id="45312-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="45312-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45312-110">PARAMETERS</span></span>

### <span data-ttu-id="45312-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="45312-111">-Context</span></span>
<span data-ttu-id="45312-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="45312-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="45312-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="45312-113">This parameter is required.</span></span>

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

### <span data-ttu-id="45312-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45312-114">-DefaultProfile</span></span>
<span data-ttu-id="45312-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45312-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45312-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45312-116">-PassThru</span></span>
<span data-ttu-id="45312-117">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="45312-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="45312-118">-Digitare</span><span class="sxs-lookup"><span data-stu-id="45312-118">-Type</span></span>
<span data-ttu-id="45312-119">Identificatore di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="45312-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="45312-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="45312-120">This parameter is required.</span></span>

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

### <span data-ttu-id="45312-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45312-121">-Confirm</span></span>
<span data-ttu-id="45312-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45312-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45312-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45312-123">-WhatIf</span></span>
<span data-ttu-id="45312-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45312-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45312-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45312-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45312-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45312-126">CommonParameters</span></span>
<span data-ttu-id="45312-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45312-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45312-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45312-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45312-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45312-129">INPUTS</span></span>

### <span data-ttu-id="45312-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="45312-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45312-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="45312-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="45312-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45312-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="45312-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45312-133">OUTPUTS</span></span>

### <span data-ttu-id="45312-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45312-134">System.Boolean</span></span>

## <span data-ttu-id="45312-135">Note</span><span class="sxs-lookup"><span data-stu-id="45312-135">NOTES</span></span>

## <span data-ttu-id="45312-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45312-136">RELATED LINKS</span></span>

[<span data-ttu-id="45312-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="45312-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="45312-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="45312-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="45312-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="45312-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)

