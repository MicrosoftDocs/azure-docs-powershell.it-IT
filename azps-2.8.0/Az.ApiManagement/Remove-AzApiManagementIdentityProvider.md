---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 538fcb0a2b275a81c76c921add422348fe461722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675941"
---
# <span data-ttu-id="03262-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="03262-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="03262-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03262-102">SYNOPSIS</span></span>
<span data-ttu-id="03262-103">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="03262-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="03262-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03262-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03262-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03262-105">DESCRIPTION</span></span>
<span data-ttu-id="03262-106">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="03262-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="03262-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03262-107">EXAMPLES</span></span>

### <span data-ttu-id="03262-108">Rimuove le impostazioni del provider di identità di Facebook dal servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="03262-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="03262-109">Elimina la configurazione relativa alla configurazione del provider di identità di Facebook.</span><span class="sxs-lookup"><span data-stu-id="03262-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="03262-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03262-110">PARAMETERS</span></span>

### <span data-ttu-id="03262-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="03262-111">-Context</span></span>
<span data-ttu-id="03262-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="03262-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="03262-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="03262-113">This parameter is required.</span></span>

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

### <span data-ttu-id="03262-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03262-114">-DefaultProfile</span></span>
<span data-ttu-id="03262-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03262-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03262-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03262-116">-PassThru</span></span>
<span data-ttu-id="03262-117">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="03262-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="03262-118">-Digitare</span><span class="sxs-lookup"><span data-stu-id="03262-118">-Type</span></span>
<span data-ttu-id="03262-119">Identificatore di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="03262-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="03262-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="03262-120">This parameter is required.</span></span>

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

### <span data-ttu-id="03262-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03262-121">-Confirm</span></span>
<span data-ttu-id="03262-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03262-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03262-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03262-123">-WhatIf</span></span>
<span data-ttu-id="03262-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03262-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03262-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03262-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03262-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03262-126">CommonParameters</span></span>
<span data-ttu-id="03262-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03262-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03262-128">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03262-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03262-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03262-129">INPUTS</span></span>

### <span data-ttu-id="03262-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="03262-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="03262-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="03262-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="03262-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03262-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="03262-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03262-133">OUTPUTS</span></span>

### <span data-ttu-id="03262-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03262-134">System.Boolean</span></span>

## <span data-ttu-id="03262-135">Note</span><span class="sxs-lookup"><span data-stu-id="03262-135">NOTES</span></span>

## <span data-ttu-id="03262-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03262-136">RELATED LINKS</span></span>

[<span data-ttu-id="03262-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="03262-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="03262-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="03262-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="03262-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="03262-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
