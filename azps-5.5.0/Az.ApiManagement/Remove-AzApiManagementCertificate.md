---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: ab1623addbb415b1aa2f6a104904629d94b518d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195358"
---
# <span data-ttu-id="721f7-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="721f7-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="721f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="721f7-102">SYNOPSIS</span></span>
<span data-ttu-id="721f7-103">Rimuove un certificato di gestione DELLE API.</span><span class="sxs-lookup"><span data-stu-id="721f7-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="721f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="721f7-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="721f7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="721f7-105">DESCRIPTION</span></span>
<span data-ttu-id="721f7-106">Il cmdlet **Remove-AzApiManagementCertificate** rimuove un certificato di Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="721f7-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="721f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="721f7-107">EXAMPLES</span></span>

### <span data-ttu-id="721f7-108">Esempio 1: Rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="721f7-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="721f7-109">Questo comando rimuove il certificato di gestione API specificato.</span><span class="sxs-lookup"><span data-stu-id="721f7-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="721f7-110">Poiché è *specificato il* parametro Force, non è necessaria alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="721f7-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="721f7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="721f7-111">PARAMETERS</span></span>

### <span data-ttu-id="721f7-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="721f7-112">-CertificateId</span></span>
<span data-ttu-id="721f7-113">Specifica l'ID del certificato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="721f7-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="721f7-114">-Context</span><span class="sxs-lookup"><span data-stu-id="721f7-114">-Context</span></span>
<span data-ttu-id="721f7-115">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="721f7-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="721f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721f7-116">-DefaultProfile</span></span>
<span data-ttu-id="721f7-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="721f7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="721f7-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="721f7-118">-PassThru</span></span>
<span data-ttu-id="721f7-119">passthru</span><span class="sxs-lookup"><span data-stu-id="721f7-119">passthru</span></span>

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

### <span data-ttu-id="721f7-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="721f7-120">-Confirm</span></span>
<span data-ttu-id="721f7-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="721f7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="721f7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="721f7-122">-WhatIf</span></span>
<span data-ttu-id="721f7-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="721f7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="721f7-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="721f7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="721f7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721f7-125">CommonParameters</span></span>
<span data-ttu-id="721f7-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721f7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721f7-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="721f7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721f7-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="721f7-128">INPUTS</span></span>

### <span data-ttu-id="721f7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="721f7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="721f7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="721f7-130">System.String</span></span>

### <span data-ttu-id="721f7-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="721f7-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="721f7-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="721f7-132">OUTPUTS</span></span>

### <span data-ttu-id="721f7-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="721f7-133">System.Boolean</span></span>

## <span data-ttu-id="721f7-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="721f7-134">NOTES</span></span>

## <span data-ttu-id="721f7-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="721f7-135">RELATED LINKS</span></span>

[<span data-ttu-id="721f7-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="721f7-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="721f7-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="721f7-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="721f7-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="721f7-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


