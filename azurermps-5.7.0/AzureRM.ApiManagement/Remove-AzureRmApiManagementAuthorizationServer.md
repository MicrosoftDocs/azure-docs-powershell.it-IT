---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: c9133c7a2924b4151afd01f257fe6b54a9eeb00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521477"
---
# <span data-ttu-id="d0f3a-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d0f3a-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="d0f3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f3a-103">Rimuove un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d0f3a-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0f3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0f3a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f3a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f3a-106">Il cmdlet **Remove-AzureRmApiManagementAuthorizationServer** rimuove un server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f3a-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="d0f3a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0f3a-107">EXAMPLES</span></span>

## <span data-ttu-id="d0f3a-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0f3a-108">PARAMETERS</span></span>

### <span data-ttu-id="d0f3a-109">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d0f3a-109">-Context</span></span>
<span data-ttu-id="d0f3a-110">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d0f3a-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d0f3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f3a-111">-DefaultProfile</span></span>
<span data-ttu-id="d0f3a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f3a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d0f3a-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0f3a-113">-PassThru</span></span>
<span data-ttu-id="d0f3a-114">PassThru</span><span class="sxs-lookup"><span data-stu-id="d0f3a-114">passthru</span></span>

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

### <span data-ttu-id="d0f3a-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="d0f3a-115">-ServerId</span></span>
<span data-ttu-id="d0f3a-116">Specifica l'ID del server di autorizzazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d0f3a-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="d0f3a-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0f3a-117">-Confirm</span></span>
<span data-ttu-id="d0f3a-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0f3a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f3a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f3a-119">-WhatIf</span></span>
<span data-ttu-id="d0f3a-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0f3a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f3a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0f3a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f3a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f3a-122">CommonParameters</span></span>
<span data-ttu-id="d0f3a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f3a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f3a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f3a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f3a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0f3a-125">INPUTS</span></span>

### <span data-ttu-id="d0f3a-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d0f3a-126">None</span></span>
<span data-ttu-id="d0f3a-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d0f3a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0f3a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0f3a-128">OUTPUTS</span></span>

### <span data-ttu-id="d0f3a-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="d0f3a-129">Boolean</span></span>

## <span data-ttu-id="d0f3a-130">Note</span><span class="sxs-lookup"><span data-stu-id="d0f3a-130">NOTES</span></span>

## <span data-ttu-id="d0f3a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0f3a-131">RELATED LINKS</span></span>

[<span data-ttu-id="d0f3a-132">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d0f3a-132">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="d0f3a-133">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d0f3a-133">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="d0f3a-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="d0f3a-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


