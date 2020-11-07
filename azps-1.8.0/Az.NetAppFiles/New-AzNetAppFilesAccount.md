---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 87febe648a845d595f35c1a14b024fbd97824be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678734"
---
# <span data-ttu-id="d6f67-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d6f67-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d6f67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6f67-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f67-103">Crea un nuovo account di Azure NetApp file (ANF).</span><span class="sxs-lookup"><span data-stu-id="d6f67-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="d6f67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6f67-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f67-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6f67-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f67-106">Il cmdlet **New-AzNetAppFilesAccount** crea un account ANF.</span><span class="sxs-lookup"><span data-stu-id="d6f67-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="d6f67-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6f67-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f67-108">Esempio 1: creare un account di ANF</span><span class="sxs-lookup"><span data-stu-id="d6f67-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="d6f67-109">Questo comando crea il nuovo account di ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="d6f67-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="d6f67-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6f67-110">PARAMETERS</span></span>

### <span data-ttu-id="d6f67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f67-111">-DefaultProfile</span></span>
<span data-ttu-id="d6f67-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f67-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f67-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d6f67-113">-Location</span></span>
<span data-ttu-id="d6f67-114">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="d6f67-114">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f67-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6f67-115">-Name</span></span>
<span data-ttu-id="d6f67-116">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="d6f67-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f67-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f67-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6f67-118">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="d6f67-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f67-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6f67-119">-Tag</span></span>
<span data-ttu-id="d6f67-120">Hashtable che rappresenta i tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="d6f67-120">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f67-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6f67-121">-Confirm</span></span>
<span data-ttu-id="d6f67-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6f67-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f67-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f67-123">-WhatIf</span></span>
<span data-ttu-id="d6f67-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6f67-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f67-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6f67-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f67-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f67-126">CommonParameters</span></span>
<span data-ttu-id="d6f67-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f67-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d6f67-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f67-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f67-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6f67-129">INPUTS</span></span>

### <span data-ttu-id="d6f67-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d6f67-130">None</span></span>

## <span data-ttu-id="d6f67-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6f67-131">OUTPUTS</span></span>

### <span data-ttu-id="d6f67-132">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d6f67-132">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d6f67-133">Note</span><span class="sxs-lookup"><span data-stu-id="d6f67-133">NOTES</span></span>

## <span data-ttu-id="d6f67-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6f67-134">RELATED LINKS</span></span>
