---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 16a48b6f945aac8ef287ff612d64da1273add521
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508820"
---
# <span data-ttu-id="7df7c-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7df7c-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="7df7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7df7c-102">SYNOPSIS</span></span>
<span data-ttu-id="7df7c-103">Rimuove un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="7df7c-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7df7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7df7c-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7df7c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7df7c-105">DESCRIPTION</span></span>
<span data-ttu-id="7df7c-106">Il cmdlet **Remove-AzureRmApiManagementAuthorizationServer** rimuove un server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="7df7c-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="7df7c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7df7c-107">EXAMPLES</span></span>

## <span data-ttu-id="7df7c-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7df7c-108">PARAMETERS</span></span>

### <span data-ttu-id="7df7c-109">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7df7c-109">-Context</span></span>
<span data-ttu-id="7df7c-110">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7df7c-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7df7c-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7df7c-111">-PassThru</span></span>
<span data-ttu-id="7df7c-112">PassThru</span><span class="sxs-lookup"><span data-stu-id="7df7c-112">passthru</span></span>

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

### <span data-ttu-id="7df7c-113">-ServerId</span><span class="sxs-lookup"><span data-stu-id="7df7c-113">-ServerId</span></span>
<span data-ttu-id="7df7c-114">Specifica l'ID del server di autorizzazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7df7c-114">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="7df7c-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7df7c-115">-Confirm</span></span>
<span data-ttu-id="7df7c-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7df7c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7df7c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7df7c-117">-WhatIf</span></span>
<span data-ttu-id="7df7c-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7df7c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7df7c-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7df7c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7df7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7df7c-120">-DefaultProfile</span></span>
<span data-ttu-id="7df7c-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7df7c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7df7c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7df7c-122">CommonParameters</span></span>
<span data-ttu-id="7df7c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7df7c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7df7c-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7df7c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7df7c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7df7c-125">INPUTS</span></span>

## <span data-ttu-id="7df7c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7df7c-126">OUTPUTS</span></span>

### <span data-ttu-id="7df7c-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="7df7c-127">Boolean</span></span>

## <span data-ttu-id="7df7c-128">Note</span><span class="sxs-lookup"><span data-stu-id="7df7c-128">NOTES</span></span>

## <span data-ttu-id="7df7c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7df7c-129">RELATED LINKS</span></span>

[<span data-ttu-id="7df7c-130">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7df7c-130">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="7df7c-131">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7df7c-131">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="7df7c-132">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7df7c-132">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


