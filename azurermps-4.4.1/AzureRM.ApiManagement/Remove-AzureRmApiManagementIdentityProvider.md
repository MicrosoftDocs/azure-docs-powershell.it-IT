---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511388"
---
# <span data-ttu-id="1bbbb-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1bbbb-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="1bbbb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="1bbbb-103">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bbbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bbbb-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bbbb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bbbb-105">DESCRIPTION</span></span>
<span data-ttu-id="1bbbb-106">Rimuove una configurazione del provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="1bbbb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bbbb-107">EXAMPLES</span></span>

### <span data-ttu-id="1bbbb-108">Rimuove le impostazioni del provider di identità di Facebook dal servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1bbbb-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="1bbbb-109">Elimina la configurazione relativa alla configurazione del provider di identità di Facebook.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="1bbbb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bbbb-110">PARAMETERS</span></span>

### <span data-ttu-id="1bbbb-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1bbbb-111">-Context</span></span>
<span data-ttu-id="1bbbb-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1bbbb-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1bbbb-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bbbb-114">-PassThru</span></span>
<span data-ttu-id="1bbbb-115">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="1bbbb-116">-Digitare</span><span class="sxs-lookup"><span data-stu-id="1bbbb-116">-Type</span></span>
<span data-ttu-id="1bbbb-117">Identificatore di un provider di identità esistente.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="1bbbb-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bbbb-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1bbbb-119">-Confirm</span></span>
<span data-ttu-id="1bbbb-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bbbb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bbbb-121">-WhatIf</span></span>
<span data-ttu-id="1bbbb-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bbbb-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bbbb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bbbb-124">-DefaultProfile</span></span>
<span data-ttu-id="1bbbb-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bbbb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bbbb-126">CommonParameters</span></span>
<span data-ttu-id="1bbbb-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bbbb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bbbb-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bbbb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bbbb-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bbbb-129">INPUTS</span></span>

## <span data-ttu-id="1bbbb-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bbbb-130">OUTPUTS</span></span>

### <span data-ttu-id="1bbbb-131">bool</span><span class="sxs-lookup"><span data-stu-id="1bbbb-131">bool</span></span>

## <span data-ttu-id="1bbbb-132">Note</span><span class="sxs-lookup"><span data-stu-id="1bbbb-132">NOTES</span></span>

## <span data-ttu-id="1bbbb-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bbbb-133">RELATED LINKS</span></span>

[<span data-ttu-id="1bbbb-134">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1bbbb-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="1bbbb-135">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1bbbb-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="1bbbb-136">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="1bbbb-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)

