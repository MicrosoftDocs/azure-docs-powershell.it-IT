---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2fc658f5bab9e6233e6b7279abc0ae80832bcc8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507759"
---
# <span data-ttu-id="164e1-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="164e1-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="164e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="164e1-102">SYNOPSIS</span></span>
<span data-ttu-id="164e1-103">Rimuove un server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="164e1-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="164e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="164e1-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="164e1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="164e1-105">DESCRIPTION</span></span>
<span data-ttu-id="164e1-106">Il cmdlet **Remove-AzureRmApiManagementAuthorizationServer** rimuove un server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="164e1-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="164e1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="164e1-107">EXAMPLES</span></span>

## <span data-ttu-id="164e1-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="164e1-108">PARAMETERS</span></span>

### <span data-ttu-id="164e1-109">-Contesto</span><span class="sxs-lookup"><span data-stu-id="164e1-109">-Context</span></span>
<span data-ttu-id="164e1-110">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="164e1-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="164e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="164e1-111">-DefaultProfile</span></span>
<span data-ttu-id="164e1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="164e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="164e1-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="164e1-113">-PassThru</span></span>
<span data-ttu-id="164e1-114">PassThru</span><span class="sxs-lookup"><span data-stu-id="164e1-114">passthru</span></span>

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

### <span data-ttu-id="164e1-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="164e1-115">-ServerId</span></span>
<span data-ttu-id="164e1-116">Specifica l'ID del server di autorizzazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="164e1-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="164e1-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="164e1-117">-Confirm</span></span>
<span data-ttu-id="164e1-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="164e1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="164e1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="164e1-119">-WhatIf</span></span>
<span data-ttu-id="164e1-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="164e1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="164e1-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="164e1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="164e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="164e1-122">CommonParameters</span></span>
<span data-ttu-id="164e1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="164e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="164e1-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="164e1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="164e1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="164e1-125">INPUTS</span></span>

### <span data-ttu-id="164e1-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="164e1-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="164e1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="164e1-127">System.String</span></span>

### <span data-ttu-id="164e1-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="164e1-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="164e1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="164e1-129">OUTPUTS</span></span>

### <span data-ttu-id="164e1-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="164e1-130">System.Boolean</span></span>

## <span data-ttu-id="164e1-131">Note</span><span class="sxs-lookup"><span data-stu-id="164e1-131">NOTES</span></span>

## <span data-ttu-id="164e1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="164e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="164e1-133">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="164e1-133">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="164e1-134">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="164e1-134">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="164e1-135">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="164e1-135">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


