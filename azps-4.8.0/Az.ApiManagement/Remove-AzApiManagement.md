---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: f54998dc0d5ec8570a573870148a8cf05c265618
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191718"
---
# <span data-ttu-id="1a55e-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1a55e-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="1a55e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a55e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a55e-103">Rimuove un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="1a55e-103">Removes an API Management service.</span></span>

## <span data-ttu-id="1a55e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a55e-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a55e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a55e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a55e-106">Il cmdlet **Remove-AzApiManagement** rimuove un servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a55e-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="1a55e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a55e-107">EXAMPLES</span></span>

### <span data-ttu-id="1a55e-108">Esempio 1: rimuovere un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="1a55e-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="1a55e-109">Questo comando rimuove il servizio di gestione delle API denominato ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="1a55e-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="1a55e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a55e-110">PARAMETERS</span></span>

### <span data-ttu-id="1a55e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a55e-111">-DefaultProfile</span></span>
<span data-ttu-id="1a55e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a55e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a55e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a55e-113">-Name</span></span>
<span data-ttu-id="1a55e-114">Specifica il nome della distribuzione di gestione delle API rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a55e-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1a55e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a55e-115">-PassThru</span></span>
<span data-ttu-id="1a55e-116">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="1a55e-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a55e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a55e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a55e-118">Specifica il nome del gruppo di risorse in cui è presente la distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="1a55e-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="1a55e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a55e-119">-Confirm</span></span>
<span data-ttu-id="1a55e-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a55e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a55e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a55e-121">-WhatIf</span></span>
<span data-ttu-id="1a55e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a55e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a55e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a55e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a55e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a55e-124">CommonParameters</span></span>
<span data-ttu-id="1a55e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a55e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a55e-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a55e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a55e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a55e-127">INPUTS</span></span>

### <span data-ttu-id="1a55e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1a55e-128">System.String</span></span>

## <span data-ttu-id="1a55e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a55e-129">OUTPUTS</span></span>

### <span data-ttu-id="1a55e-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a55e-130">System.Boolean</span></span>

## <span data-ttu-id="1a55e-131">Note</span><span class="sxs-lookup"><span data-stu-id="1a55e-131">NOTES</span></span>

## <span data-ttu-id="1a55e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a55e-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a55e-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1a55e-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="1a55e-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1a55e-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="1a55e-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1a55e-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="1a55e-136">Ripristinare-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1a55e-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)

