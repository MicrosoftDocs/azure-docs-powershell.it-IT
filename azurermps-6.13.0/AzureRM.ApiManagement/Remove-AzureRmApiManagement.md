---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: cee512445f457e7353d5766cd561788b00360b40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687385"
---
# <span data-ttu-id="3a856-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a856-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="3a856-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a856-102">SYNOPSIS</span></span>
<span data-ttu-id="3a856-103">Rimuove un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="3a856-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a856-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a856-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a856-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a856-105">DESCRIPTION</span></span>
<span data-ttu-id="3a856-106">Il cmdlet **Remove-AzureRmApiManagement** rimuove un servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="3a856-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="3a856-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a856-107">EXAMPLES</span></span>

### <span data-ttu-id="3a856-108">Esempio 1: rimuovere un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="3a856-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="3a856-109">Questo comando rimuove il servizio di gestione delle API denominato ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="3a856-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="3a856-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a856-110">PARAMETERS</span></span>

### <span data-ttu-id="3a856-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a856-111">-DefaultProfile</span></span>
<span data-ttu-id="3a856-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a856-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a856-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a856-113">-Name</span></span>
<span data-ttu-id="3a856-114">Specifica il nome della distribuzione di gestione delle API rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a856-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a856-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a856-115">-PassThru</span></span>
<span data-ttu-id="3a856-116">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="3a856-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="3a856-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a856-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a856-118">Specifica il nome del gruppo di risorse in cui è presente la distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="3a856-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="3a856-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a856-119">-Confirm</span></span>
<span data-ttu-id="3a856-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a856-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a856-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a856-121">-WhatIf</span></span>
<span data-ttu-id="3a856-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a856-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a856-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a856-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a856-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a856-124">CommonParameters</span></span>
<span data-ttu-id="3a856-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a856-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a856-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a856-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a856-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a856-127">INPUTS</span></span>

### <span data-ttu-id="3a856-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3a856-128">System.String</span></span>

## <span data-ttu-id="3a856-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a856-129">OUTPUTS</span></span>

### <span data-ttu-id="3a856-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a856-130">System.Boolean</span></span>

## <span data-ttu-id="3a856-131">Note</span><span class="sxs-lookup"><span data-stu-id="3a856-131">NOTES</span></span>

## <span data-ttu-id="3a856-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a856-132">RELATED LINKS</span></span>

[<span data-ttu-id="3a856-133">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a856-133">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="3a856-134">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a856-134">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="3a856-135">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a856-135">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="3a856-136">Ripristinare-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a856-136">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


