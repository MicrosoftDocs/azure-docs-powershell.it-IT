---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 6e3803b7627e16a96c8101f3a6dd1eee5a1b2689
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863513"
---
# <span data-ttu-id="94a49-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="94a49-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="94a49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94a49-102">SYNOPSIS</span></span>
<span data-ttu-id="94a49-103">Rimuove un'estensione di SQL Server da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="94a49-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="94a49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94a49-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94a49-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94a49-105">DESCRIPTION</span></span>
<span data-ttu-id="94a49-106">Il cmdlet **Remove-AzVMSqlServerExtension** rimuove un'estensione del server AzureSQL da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="94a49-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="94a49-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94a49-107">EXAMPLES</span></span>

### <span data-ttu-id="94a49-108">Esempio 1: rimuovere un'estensione di SQL Server</span><span class="sxs-lookup"><span data-stu-id="94a49-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="94a49-109">Questo comando rimuove un'estensione di SQL Server dalla macchina virtuale denominata ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="94a49-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="94a49-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94a49-110">PARAMETERS</span></span>

### <span data-ttu-id="94a49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a49-111">-DefaultProfile</span></span>
<span data-ttu-id="94a49-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94a49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94a49-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="94a49-113">-Name</span></span>
<span data-ttu-id="94a49-114">Specifica il nome di SQL Server che viene rimosso dall'estensione di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94a49-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a49-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a49-115">-ResourceGroupName</span></span>
<span data-ttu-id="94a49-116">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="94a49-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a49-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="94a49-117">-VMName</span></span>
<span data-ttu-id="94a49-118">Specifica il nome della macchina virtuale da cui questo cmdlet rimuove l'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="94a49-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a49-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a49-119">CommonParameters</span></span>
<span data-ttu-id="94a49-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94a49-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a49-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94a49-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a49-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94a49-122">INPUTS</span></span>

### <span data-ttu-id="94a49-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="94a49-123">None</span></span>
<span data-ttu-id="94a49-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="94a49-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94a49-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94a49-125">OUTPUTS</span></span>

### <span data-ttu-id="94a49-126">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="94a49-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="94a49-127">Note</span><span class="sxs-lookup"><span data-stu-id="94a49-127">NOTES</span></span>

## <span data-ttu-id="94a49-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94a49-128">RELATED LINKS</span></span>

[<span data-ttu-id="94a49-129">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="94a49-129">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="94a49-130">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="94a49-130">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


