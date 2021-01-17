---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475592"
---
# <span data-ttu-id="90fb9-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="90fb9-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="90fb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="90fb9-103">Eliminare l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="90fb9-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="90fb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90fb9-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90fb9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90fb9-105">DESCRIPTION</span></span>
<span data-ttu-id="90fb9-106">Eliminare l'ID Microsoft Partner Network (MPN) dell'utente o dell'entità di servizio corrente autenticato.</span><span class="sxs-lookup"><span data-stu-id="90fb9-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="90fb9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90fb9-107">EXAMPLES</span></span>

### <span data-ttu-id="90fb9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="90fb9-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="90fb9-109">Rimuovi partner di gestione</span><span class="sxs-lookup"><span data-stu-id="90fb9-109">Remove management partner</span></span>

## <span data-ttu-id="90fb9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90fb9-110">PARAMETERS</span></span>

### <span data-ttu-id="90fb9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90fb9-111">-DefaultProfile</span></span>
<span data-ttu-id="90fb9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90fb9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90fb9-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="90fb9-113">-PartnerId</span></span>
<span data-ttu-id="90fb9-114">L'ID del partner di gestione è un numero a 6 cifre</span><span class="sxs-lookup"><span data-stu-id="90fb9-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90fb9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90fb9-115">-PassThru</span></span>
<span data-ttu-id="90fb9-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="90fb9-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="90fb9-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90fb9-117">-Confirm</span></span>
<span data-ttu-id="90fb9-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90fb9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90fb9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90fb9-119">-WhatIf</span></span>
<span data-ttu-id="90fb9-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90fb9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90fb9-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90fb9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90fb9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90fb9-122">CommonParameters</span></span>
<span data-ttu-id="90fb9-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90fb9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90fb9-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90fb9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90fb9-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90fb9-125">INPUTS</span></span>

### <span data-ttu-id="90fb9-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="90fb9-126">None</span></span>

## <span data-ttu-id="90fb9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90fb9-127">OUTPUTS</span></span>

### <span data-ttu-id="90fb9-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90fb9-128">System.Boolean</span></span>

## <span data-ttu-id="90fb9-129">Note</span><span class="sxs-lookup"><span data-stu-id="90fb9-129">NOTES</span></span>

## <span data-ttu-id="90fb9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90fb9-130">RELATED LINKS</span></span>

[<span data-ttu-id="90fb9-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="90fb9-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="90fb9-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="90fb9-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="90fb9-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="90fb9-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)