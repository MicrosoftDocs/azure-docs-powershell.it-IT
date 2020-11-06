---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: 03f56a17d038407b3a33c09188c9a29b6f4caf09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511396"
---
# <span data-ttu-id="aad05-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aad05-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="aad05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aad05-102">SYNOPSIS</span></span>
<span data-ttu-id="aad05-103">Rimuove un backend.</span><span class="sxs-lookup"><span data-stu-id="aad05-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aad05-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad05-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aad05-105">DESCRIPTION</span></span>
<span data-ttu-id="aad05-106">Rimuove un backend specificato dall'identificatore dalla gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="aad05-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="aad05-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aad05-107">EXAMPLES</span></span>

### <span data-ttu-id="aad05-108">Esempio 1: rimuovere il backend 123</span><span class="sxs-lookup"><span data-stu-id="aad05-108">Example 1: Remove the Backend 123</span></span>
```
Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="aad05-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aad05-109">PARAMETERS</span></span>

### <span data-ttu-id="aad05-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="aad05-110">-BackendId</span></span>
<span data-ttu-id="aad05-111">Identificatore del backend esistente.</span><span class="sxs-lookup"><span data-stu-id="aad05-111">Identifier of existing backend.</span></span>
<span data-ttu-id="aad05-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="aad05-112">This parameter is required.</span></span>

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

### <span data-ttu-id="aad05-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="aad05-113">-Context</span></span>
<span data-ttu-id="aad05-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="aad05-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aad05-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="aad05-115">This parameter is required.</span></span>

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

### <span data-ttu-id="aad05-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aad05-116">-PassThru</span></span>
<span data-ttu-id="aad05-117">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="aad05-117">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="aad05-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="aad05-118">This parameter is optional.</span></span>
<span data-ttu-id="aad05-119">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="aad05-119">Default value is false.</span></span>

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

### <span data-ttu-id="aad05-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aad05-120">-Confirm</span></span>
<span data-ttu-id="aad05-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad05-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aad05-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad05-122">-WhatIf</span></span>
<span data-ttu-id="aad05-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aad05-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aad05-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aad05-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aad05-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad05-125">-DefaultProfile</span></span>
<span data-ttu-id="aad05-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aad05-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aad05-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad05-127">CommonParameters</span></span>
<span data-ttu-id="aad05-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad05-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad05-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad05-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad05-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aad05-130">INPUTS</span></span>

## <span data-ttu-id="aad05-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aad05-131">OUTPUTS</span></span>

### <span data-ttu-id="aad05-132">bool</span><span class="sxs-lookup"><span data-stu-id="aad05-132">bool</span></span>

## <span data-ttu-id="aad05-133">Note</span><span class="sxs-lookup"><span data-stu-id="aad05-133">NOTES</span></span>

## <span data-ttu-id="aad05-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aad05-134">RELATED LINKS</span></span>

[<span data-ttu-id="aad05-135">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aad05-135">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="aad05-136">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aad05-136">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="aad05-137">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="aad05-137">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="aad05-138">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="aad05-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="aad05-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aad05-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
